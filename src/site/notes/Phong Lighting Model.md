---
{"dg-publish":true,"permalink":"/phong-lighting-model/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

#graphics 
> [[CS250 Hub - Graphics II|CS250 Hub - Graphics II]]

The color a viewer sees from the point $P$ is given by:
$$
\begin{align*}
&C(P)= k_{diff} (\vec{m}\cdot\vec{L})C_{light}+k_{spec}(\vec{R}_{L}\cdot\vec{v})^{n_{spec}} C_{light} + k_{diff}C_{amb} \\
&\qquad\qquad\qquad\quad\uparrow \qquad\qquad\qquad\qquad\uparrow
\qquad\qquad\qquad\qquad \uparrow\\
&\qquad\qquad\text{normalized} \qquad\qquad \text{normalized*}
\qquad\text{"ambient light term"}\\
\end{align*}
$$
It's basically the combined [[Diffuse Reflection Model|Diffuse Reflection Model]] and [[Phong Specular Reflection Model|Phong Specular Reflection Model]]!

\* those other conditions found in [[Phong Specular Reflection Model|Phong Specular Reflection Model]] apply as well
