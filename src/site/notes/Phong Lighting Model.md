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

We can view it as:
$$
C(P) = C_{amb}(P) + C_{diff}(P)+ C_{spec}(P)
$$
Where:
$$
\begin{align*}
&C_{amb}(P) = k_{diff}C_{amb}\\
&C_{diff}(P) = \text{Col. due to diffuse refl.} = k_{diff}\textcolor{orange}{(\vec{m}\cdot\vec{L})} C_{light}\\
&C_{spec}(P)= \text{Col. due to spec. refl.} = k_{spec}\textcolor{orange}{(\vec{R}_{L}\cdot\vec{v})}^{n_{spec}}C_{light}
\end{align*}
$$

$\textcolor{orange}{ * \text{Restrictions}:}$ Restrictions found in [[Phong Specular Reflection Model|Phong Specular Reflection Model]] and [[Diffuse Reflection Model|Diffuse Reflection Model]]

That ambient light term is a very rough approximation of [[Local and Global Illumination|global illumination]].