---
{"dg-publish":true,"permalink":"/me/modding/spiderman-remastered/toc-file-decompression-and-parsing/","dgHomeLink":true,"dgPassFrontmatter":false}
---

#cs #modding 
> [[🌟 Me/Modding/Spiderman Remastered/Spiderman Remastered Hub|Spiderman Remastered Hub]]

Location: `asset_archive\toc`

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