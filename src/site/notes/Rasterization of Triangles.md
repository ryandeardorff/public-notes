---
{"dg-publish":true,"permalink":"/rasterization-of-triangles/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

#graphics 
> [[CS200 Hub - Computer Graphics I|CS200 Hub - Computer Graphics I]]

- Verts of $\triangle P Q R$
	- Note: verts are not necessarily located at pixels
- Goal: Set all pixels within and (for now) exactly on the boundary.

We will do this by using [[Barycentric Coordinates|Barycentric Coordinates]], specifically [[Barycentric Coordinates with 3 Points|Barycentric Coordinates with 3 Points]].