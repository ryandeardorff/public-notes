---
{"dg-publish":true,"permalink":"/swizzling-vectors/","dgHomeLink":true,"dgPassFrontmatter":false}
---

#cs #graphics 
> [[CS200 Hub - Computer Graphics I|CS200 Hub - Computer Graphics I]]

Swizzling a vector in glsl is a way to get portions of a vector:

```glsl
vec4 vec_a = (1,0,0,1);
vec2 vec_b = vec_a.xy;
```

> In computer graphics, swizzling is the ability to compose vectors by arbitrarily rearranging and combining components of other vectors.
[wikipedia](https://en.wikipedia.org/wiki/Swizzling_(computer_graphics))