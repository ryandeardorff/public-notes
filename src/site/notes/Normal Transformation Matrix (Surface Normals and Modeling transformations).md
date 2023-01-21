---
{"dg-publish":true,"permalink":"/normal-transformation-matrix-surface-normals-and-modeling-transformations/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

#graphics 
> [[CS250 Hub - Graphics II|CS250 Hub - Graphics II]], [[Modeling Transformation (object-to-world)|Modeling Transformation (object-to-world)]], [[Counterclockwise Wind|Counterclockwise Wind]], [[Orientation of Triangles (normal vector)|Orientation of Triangles (normal vector)]]

### The Problem:
Suppose $M_{o}$ is the [[Modeling Transformation (object-to-world)|Modeling Transformation (object-to-world)]].
- For a vertex $P$ in object space, $M_{o}(P)$ is the corresponding point in [[Graphics Spaces|world space]].
- For surface normal $\vec{m}$ at $P$, corresponding surface normal in world space is .......?
	- It's **NOT** $\vec{m}' = M_{o}(\vec{m})$!!! They **don't transform under the modeling transformation**. Wild!
		- In general, $M_{o}(\vec{m}) = L(\vec{m})$ is not $\perp$ to surface $P'=M_{o}(P)$

# What we do:
The correct transformation of surface normals is:

If $M_{0} = T_{\vec{v}}\circ L$, then:
$$
\boxed{\vec{m}' = (L^{-1})^{\mathsf{T}}\vec{m}}
$$
