---
{"dg-publish":true,"permalink":"/me/modding/spiderman-remastered/toc-file-decompression-and-parsing/","dgHomeLink":true,"dgPassFrontmatter":false}
---

#cs #modding 
> [[🌟 Me/Modding/Spiderman Remastered/Spiderman Remastered Hub|Spiderman Remastered Hub]]

* Location: `asset_archive\toc`
* There's some great [work done by doesthisusername](https://github.com/doesthisusername/ig-tools) that helped a ton in figuring out the toc file layout.

### Decompression:
toc and dag files use zlib compression, which is really easy to decompress.

```ad-example
title: Simple Decompression Script
collapse: true
``` python
# Based on the work of https://github.com/doesthisusername/ig-tools
# and the zlib tutorial: https://stackabuse.com/python-zlib-library-tutorial/
from array import array
from io import BufferedReader, BufferedWriter, FileIO
import pathlib
from re import I
import zlib


# decompresses the provided "toc" file to the output path
def decompress_toc(path, out_path):
    # open the file reading as binary
    with open(path, "rb") as f, open(out_path, "wb") as out_f:
        zlib_decomp(f, out_f, 0x08)
        print("Finished decompressing toc file, output is at {}".format(out_path))


# decompresses the provided "dag" file
def decompress_dag(path, out_path):
    # open the file reading as binary
    with open(path, "rb") as f, open(out_path, "wb") as out_f:
        zlib_decomp(f, out_f, 0x0C)
        print("Finished decompressing dag file, output is at {}".format(out_path))


# the internal function used for decompressing with zlib-- common across toc and dag files.
def zlib_decomp(file: BufferedReader, out_file: BufferedWriter, seek_offset: int):
    # set up the zlib decompression
	# adding `32` to `windowBits` will trigger header detection
    # https://stackoverflow.com/a/22311297
    dec_obj = zlib.decompressobj(zlib.MAX_WBITS | 32)

    # init bytes for decompressed data
    data = bytes(0)

    # seek ahead number of bytes specified
    file.seek(seek_offset, 0)

    # read the bytes into memory
    buf: bytes = file.read()

    # decompress the data
    data = dec_obj.decompress(buf)
    # flush the remaining data
    data += dec_obj.flush()

    out_file.write(data)


if __name__ == '__main__':
    if not pathlib.Path("./toc.dec").exists():
        decompress_toc("toc", "toc.dec")
    if not pathlib.Path("./dag.dec").exists():
        decompress_dag("dag", "dag.dec")

```

### Parsing
- The existing work done [here](https://github.com/doesthisusername/ig-tools) has a file in there that describes the layout of toc files via [Kaitai Struct](https://kaitai.io/) which is fairly easy to translate to other languages and tools.
- I have a [ImHex](https://imhex.werwolv.net/) pattern that I put together to make it easier to see the structure of toc files with highlighting based on that Kaitai Struct file, that's available below:

>[!EXAMPLE]- ImHex Pattern
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
> } [[static|static]];
> 
> struct ArchiveFile{
	> u16 unknown_0;
	> u8 install_bucket;
	> u8 unknown;
	> u32 chunkmap;
	> char filename[0x10];
	> padding[0x18*2];
> } [[static|static]];
> 
> struct SpanEntry{
	> u32 asset_index [[color("005FFF")|color("005FFF")]];
	> u32 count [[color("008F8F")|color("008F8F")]];
> } [[static|static]];
> 
> struct AssetId{
	> u64 built_hash;
> } [[static|static]];
> 
> struct KeyAsset{
	> u32 assed_id;
> } [[static|static]];
> 
> struct SizeEntry{
	> u32 file_ctr_inc;
	> u32 file_size;
	> u32 file_ctr;
> } [[static|static]];
> 
> struct OffsetEntry{
	> u32 archive_index;
	> u32 archive_offset;
> } [[static|static]];
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
> } [[static|static]];
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

```ad-example 
title:Basic Parsing Script
collapse:true
```python
from __future__ import annotations
from io import IOBase


def read_u8(bin: IOBase) -> int:
    return int.from_bytes(bin.read(0x01), 'little', signed=False)


def read_u16(bin: IOBase) -> int:
    return int.from_bytes(bin.read(0x02), 'little', signed=False)


def read_u32(bin: IOBase) -> int:
    return int.from_bytes(bin.read(0x04), 'little', signed=False)


def read_u64(bin: IOBase) -> int:
    return int.from_bytes(bin.read(0x08), 'little', signed=False)


def read_str_padded(bin: IOBase) -> str:
    return bin.read(0x10).split(b'\0')[0].decode('utf-8')


class TocHeaderSect:
    def __init__(self):
        self.const_hash: bytes = b"0"
        self.offset: int = 0
        self.len: int = 0

    def read(self, bin: IOBase) -> TocHeaderSect:
        self.const_hash = bin.read(0x04)
        self.offset = read_u32(bin)
        self.len = read_u32(bin)
        return self


class ArchiveFile:
    def __init__(self):
        self.unknown_0: bytes = b"0"
        self.install_bucket: int = 0
        self.unknown_1: bytes = b"0"
        self.chunkmap: bytes = b"0"
        self.filename: str = ""
        # Padding of [0x18*2] -- the size of 2 'ArchiveFile's

    def read(self, bin: IOBase) -> ArchiveFile:
        self.unknown_0 = bin.read(0x2)
        self.install_bucket = read_u8(bin)
        self.unknown_1 = bin.read(0x1)
        self.chunkmap = bin.read(0x4)
        self.filename = read_str_padded(bin)
        # padding
        bin.read(0x18*2)

        return self

    @classmethod
    def byte_size(cls) -> int:
        return 0x48


class AssetId:
    def __init__(self):
        self.built_hash: bytes = b"0"

    def read(self, bin) -> AssetId:
        self.built_hash = bin.read(0x08)
        return self

    @classmethod
    def byte_size(cls) -> int:
        return 0x08


class SizeEntry:
    def __init__(self):
        self.file_ctr_inc: int = 0
        self.file_size: int = 0
        self.file_ctr: int = 0

    def read(self, bin: IOBase) -> SizeEntry:
        self.file_ctr_inc = read_u32(bin)
        self.file_size = read_u32(bin)
        self.file_ctr = read_u32(bin)
        return self

    @classmethod
    def byte_size(cls) -> int:
        return 0x0C


# Key assets are typically zone files evidentially
class KeyAsset:
    def __init__(self):
        self.asset_id: int = 0

    def read(self, bin: IOBase) -> KeyAsset:
        self.asset_id = read_u32(bin)
        return self

    @classmethod
    def byte_size(cls) -> int:
        return 0x04


class OffsetEntry:
    def __init__(self):
        self.archive_index: int = 0
        self.archive_offset: int = 0

    def read(self, bin: IOBase) -> OffsetEntry:
        self.archive_index = read_u32(bin)
        self.archive_offset = read_u32(bin)
        return self

    @classmethod
    def byte_size(cls) -> int:
        return 0x08


class SpanEntry:
    def __init__(self):
        self.asset_index: int = 0
        self.count: int = 0

    def read(self, bin: IOBase) -> SpanEntry:
        self.asset_index = read_u32(bin)
        self.count = read_u32(bin)
        return self

    @classmethod
    def byte_size(cls) -> int:
        return 0x08


class TocHeader:
    def __init__(self):
        self.dat1: bytes = b"0"
        self.toc_const: int = 0
        self.len_file: int = 0
        self.num_sections: int = 0
        self.archive_files_hdr = TocHeaderSect()
        self.asset_ids_hdr = TocHeaderSect()
        self.sizes_hdr = TocHeaderSect()
        self.key_assets_hdr = TocHeaderSect()
        self.offsets_hdr = TocHeaderSect()
        self.spans_hdr = TocHeaderSect()
        self.file_type_str: str = ""

    def read(self, bin):
        self.dat1 = bin.read(0x04)
        self.toc_const = read_u32(bin)
        self.len_file = read_u32(bin)
        self.num_sections = read_u32(bin)
        self.archive_files_hdr.read(bin)
        self.asset_ids_hdr.read(bin)
        self.sizes_hdr.read(bin)
        self.key_assets_hdr.read(bin)
        self.offsets_hdr.read(bin)
        self.spans_hdr.read(bin)
        self.file_type_str = read_str_padded(bin)
        return self


class TocFile:
    # path assumes a decompressed toc file
    def __init__(self, path):
        with open(path, "rb") as f:
            self.header = TocHeader().read(f)

            # Read archive files
            f.seek(self.header.archive_files_hdr.offset)
            count = self.header.archive_files_hdr.len//ArchiveFile.byte_size()
            self.archive_files = [ArchiveFile().read(f)
                                  for _i in range(0, count)]

            # Read asset ids
            f.seek(self.header.asset_ids_hdr.offset)
            count = self.header.asset_ids_hdr.len//AssetId.byte_size()
            self.asset_ids = [AssetId().read(f) for _i in range(0, count)]

            # read sizes
            f.seek(self.header.sizes_hdr.offset)
            count = self.header.sizes_hdr.len//SizeEntry.byte_size()
            self.sizes = [SizeEntry().read(f) for _i in range(0, count)]

            # read key assets
            f.seek(self.header.key_assets_hdr.offset)
            count = self.header.key_assets_hdr.len//KeyAsset.byte_size()
            self.key_assets = [KeyAsset().read(f) for _i in range(0, count)]

            # read offsets
            f.seek(self.header.offsets_hdr.offset)
            count = self.header.offsets_hdr.len//OffsetEntry.byte_size()
            self.offsets = [OffsetEntry().read(f) for _i in range(0, count)]

            # read spans
            f.seek(self.header.spans_hdr.offset)
            count = self.header.spans_hdr.len//SpanEntry.byte_size()
            self.spans = [SpanEntry().read(f) for _i in range(0, count)]


if __name__ == '__main__':
    tocfile = TocFile("toc.dec")

```