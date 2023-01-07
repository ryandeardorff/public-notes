---
{"dg-publish":true,"permalink":"/pixel-size-and-scan-line-stride/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

#graphics 
> [[CS200 Hub - Computer Graphics I|CS200 Hub - Computer Graphics I]]

We will use a 24-bit RGB color model (there are others though)
- 1 byte per color component (3 bytes total)
- Components stored in RGB order.

Some devices require that scan lines be a multiple of 4 bytes (start on a 4-byte boundary), or possibly even 8 bytes. 

This means that they may require *additional padding bytes*.

\# of bytes per scan line is called the **stride**.