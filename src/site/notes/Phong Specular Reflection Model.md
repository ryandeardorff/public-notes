---
{"dg-publish":true,"permalink":"/phong-specular-reflection-model/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

#graphics 
> [[CS250 Hub - Graphics II|CS250 Hub - Graphics II]], [[Specular Reflection|Specular Reflection]], [[Lighting|Lighting]], [[Lighting Geometry|Lighting Geometry]]

$$
C_{spec}(P) = k_{spec}\cdot (\vec{R}_{L}\cdot \vec{V})^{n_{spec}}\cdot C_{light} = k_{spec}\cdot\nu\cdot C_{light}
$$
Where:
- $k_{spec}$ = specular reflection coefficient
	- Fraction of light (at normal incidence) that is specularly reflected
	- $RGB$
- $n_{spec}$ = specular reflection exponent
- $\vec{R}_{L}$ = direction of perfect specular reflection, see [[Specular Reflection|Specular Reflection]]
*the remaining values are the same as: [[Diffuse Reflection Model|Diffuse Reflection Model]] and [[Lighting Geometry|Lighting Geometry]]*
- assumes $\vec{R}_{L}, \vec{V}$ are unit vectors
- In general, the specular shading factor ($\nu$) is:
$$
\nu = \begin{cases}
\left( \frac{\vec{R}_{L}\cdot\vec{V}}{\|\vec{R}_{L}\|\cdot \|\vec{V}\|} \right)^{n_{spec}},  & \vec{R}_{L}\cdot\vec{V} > 0 &  and  & \vec{m}\cdot\vec{L} > 0  \\
0, &\text{otherwise}
\end{cases}
$$