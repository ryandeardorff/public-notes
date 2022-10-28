---
{"dg-publish":true,"permalink":"/u-substitution-integrals/","dgHomeLink":true,"dgPassFrontmatter":false}
---

#math 
> [[MAT 150 Hub|MAT 150 Hub]]

Related to [[Integrals as the opposite of differentials|Integrals as the opposite of differentials]]

$$
\begin{align}
&\quad \quad \textcolor{orange}u\\
&\quad \quad \textcolor{orange}\downarrow\\
&\int e^{\textcolor{orange}{2x}} dx
\end{align}
$$

$$
\begin{align}
u &= 2x \\
\text{Get }&\textbf{everything }\text{in the integral in terms of } u\text{ (no } x ). \\
&\downarrow \\
&dx
\end{align}
$$

$$
\begin{align}
\frac{du}{dx} &= 2 \\
du &= 2dx \\
dx = \frac{1}{2}du &= \frac{1}{u'}du
\end{align}
$$

$$
\begin{align}
\int e ^{2x} dx = \int e^{2x} \left(\frac{1}{2}du\right) = \int e^{u} \frac{1}{2}du = \frac{1}{2}\int e^{u} du = \frac{1}{2}(e^{u}+C_{1}) = \frac{1}{2}e ^{u} +C_{2} \\
=\boxed{\frac{1}{2}e^{2x}+C}
\end{align}
$$

We're reinterpreting how we traverse the function, in this case it was traversing twice as fast.