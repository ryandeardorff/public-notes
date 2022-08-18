---
{"dg-publish":true,"permalink":"/me/modding/spiderman-remastered/toc-file-decompression-and-parsing/","dgHomeLink":true,"dgPassFrontmatter":false}
---

#cs #modding 
> [[🌟 Me/Modding/Spiderman Remastered/Spiderman Remastered Hub|Spiderman Remastered Hub]]

* Location: `asset_archive\toc`

### Decompression:
toc and dag files use zlib compression, which is really easy to decompress.

> [!EXAMPLE]- Simple Decompression Script
> ```python
> # Based on the work of https://github.com/doesthisusername/ig-tools
> # and the zlib tutorial: https://stackabuse.com/python-zlib-library-tutorial/
> from array import array
> from io import BufferedReader, BufferedWriter, FileIO
> import pathlib
> from re import I
> import zlib
> 
> 
> # decompresses the provided "toc" file to the output path
> def decompress_toc(path, out_path):
    > # open the file reading as binary
    > with open(path, "rb") as f, open(out_path, "wb") as out_f:
        > zlib_decomp(f, out_f, 0x08)
        > print("Finished decompressing toc file, output is at {}".format(out_path))
> 
> 
> # decompresses the provided "dag" file
> def decompress_dag(path, out_path):
    > # open the file reading as binary
    > with open(path, "rb") as f, open(out_path, "wb") as out_f:
        > zlib_decomp(f, out_f, 0x0C)
        > print("Finished decompressing dag file, output is at {}".format(out_path))
> 
> 
> # the internal function used for decompressing with zlib-- common across toc and dag files.
> def zlib_decomp(file: BufferedReader, out_file: BufferedWriter, seek_offset: int):
    > # set up the zlib decompression
    > # adding `32` to `windowBits` will trigger header detection
    > # https://stackoverflow.com/a/22311297
    > dec_obj = zlib.decompressobj(zlib.MAX_WBITS | 32)
> 
    > # init bytes for decompressed data
    > data = bytes(0)
> 
    > # seek ahead number of bytes specified
    > file.seek(seek_offset, 0)
> 
    > # read the bytes into memory
    > buf: bytes = file.read()
> 
    > # decompress the data
    > data = dec_obj.decompress(buf)
    > # flush the remaining data
    > data += dec_obj.flush()
> 
    > out_file.write(data)
> 
> 
> if __name__ == '__main__':
    > if not pathlib.Path("./toc.dec").exists():
        > decompress_toc("toc", "toc.dec")
    > if not pathlib.Path("./dag.dec").exists():
        > decompress_dag("dag", "dag.dec")
> ```

### Parsing
- There's some existing work done here: https://github.com/doesthisusername/ig-tools that has a file in there that describes the layout of toc files via [Kaitai Struct](https://kaitai.io/) which is fairly easy to translate to other languages and tools.
- I have a [ImHex](https://imhex.werwolv.net/) pattern that I put together to make it easier to see the structure of toc files available below:
>[!EXAMPLE]-
  >```c
  >
  >#include <std/io.pat>
> #include <std/mem.pat>
> 
> struct HeaderSect{
	> u32 const_hash;
	> u32 offset;
	> 
	> u32 len;
> } [[static]];
> 
> struct ArchiveFile{
	> u16 unknown_0;
	> u8 install_bucket;
	> u8 unknown;
	> u32 chunkmap;
	> char filename[0x10];
	> padding[0x18*2];
> } [[static]];
> 
> struct SpanEntry{
	> u32 asset_index [[color("005FFF")]];
	> u32 count [[color("008F8F")]];
> } [[static]];
> 
> struct AssetId{
	> u64 built_hash;
> } [[static]];
> 
> struct KeyAsset{
	> u32 assed_id;
> } [[static]];
> 
> struct SizeEntry{
	> u32 file_ctr_inc;
	> u32 file_size;
	> u32 file_ctr;
> } [[static]];
> 
> struct OffsetEntry{
	> u32 archive_index;
	> u32 archive_offset;
> } [[static]];
	> 
> struct Header{
	> u32 dat1;
	> u32 toc_const;
	> u32 len_file;
	> u32 num_sections;
	> HeaderSect archive_files_hdr;
	> HeaderSect asset_ids_hdr;
	> HeaderSect sizes_hdr;
	> HeaderSect key_assets_hdr;
	> HeaderSect offsets_hdr;
	> HeaderSect spans_hdr;
	> char file_type_str[24];
> } [[static]];
> 
> ArchiveFile af_size_ref;
> SpanEntry se_size_ref;
> AssetId aid_size_ref;
> KeyAsset ka_size_ref;
> SizeEntry sze_size_ref;
> OffsetEntry oe_size_ref;
> struct TOCFILE{
	> Header header;
	> ArchiveFile archive_files[header.archive_files_hdr.len / sizeof(af_size_ref)] @ header.archive_files_hdr.offset;
	> SpanEntry span_entries[header.spans_hdr.len / sizeof(se_size_ref)] @ header.spans_hdr.offset;
	> AssetId asset_ids[header.asset_ids_hdr.len / sizeof(aid_size_ref)] @ header.asset_ids_hdr.offset;
	> KeyAsset key_assets[header.key_assets_hdr.len/sizeof(ka_size_ref)] @ header.key_assets_hdr.offset;
	> SizeEntry sizes[header.sizes_hdr.len/sizeof(sze_size_ref)] @ header.sizes_hdr.offset;
	> OffsetEntry offsets[header.offsets_hdr.len/sizeof(oe_size_ref)] @ header.offsets_hdr.offset;
> };
> 
> TOCFILE toc @0x00;
> ```

* 
