---
{"dg-publish":true,"permalink":"/elementary-raster-operations/","dgHomeLink":true,"dgPassFrontmatter":false}
---

#graphics 
> [[CS200 Hub - Computer Graphics I|CS200 Hub - Computer Graphics I]], [[Rasterization|Rasterization]]

These are the operations we allow ourselves to use when doing [[Rasterization|Rasterization]].

- `setColor(c)` -- sets the current color stored internally (not drawing anything yet!)-- pen color if you will.
- `gotoPoint(i,j)` -- sets the current pixel location to $(i,j)$ (not drawing anything yet!)
- `writePixel()` -- writes the current color to the current pixel location in the frame buffer.

Those first two set up the call to the last one.

Note: `gotoPoint` will need to [[Frame Buffer Offset Calculation|compute the offset into the framebuffer]].