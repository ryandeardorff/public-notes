---
{"dg-publish":true,"permalink":"/diffuse-reflection-model/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

#graphics 
> [[CS250 Hub - Graphics II|CS250 Hub - Graphics II]], [[Diffuse Reflection|Diffuse Reflection]]

$$
C_{diff}(P) = k_{diff} (\vec{m}_{_{P}} \cdot \vec{L})C_{light}
$$

$$
C_{diff}(P) = k_{diff} \cdot \mu \cdot  C_{light}
$$

Where:
- $k_{diff}$ = difference reflection coefficient, fraction of light (at normal incidence) that is diffusely reflected by the surface (at $P$). -- ($RGB$)
- $C_{light}$ = color of light source -- ($RGB$)
- $\mu = (\vec{m}_{P}\cdot\vec{L})$ = diffuse shading factor
	- Assumes $\vec{m}_{p}$ and $\vec{L}$ are **unit** vectors.
	- If they are NOT unit vectors, then our diffuse shading factor will need to be normalized. [[Unit Vectors|Unit Vectors]].
	- In general:
$$
\mu = \begin{cases}
\vec{m_{P}}\cdot\vec{L}, & \vec{m}_{p} \cdot \vec{L} > 0 \\
\quad0, & \vec{m}_{p}\cdot\vec{L} \le 0
\end{cases}
$$
