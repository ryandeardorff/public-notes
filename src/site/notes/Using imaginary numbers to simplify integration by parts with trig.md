---
{"dg-publish":true,"permalink":"/using-imaginary-numbers-to-simplify-integration-by-parts-with-trig/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

#math 
> [[MAT 200 Hub - Calc II|MAT 200 Hub - Calc II]], [[Integration by Parts|Integration by Parts]], [[Connection between imaginary numbers and trig functions|Connection between imaginary numbers and trig functions]]

$$
\begin{align}
\int e ^ {2x}\cos x \, dx &= \int e^{2x} \frac{e^{ix}+e^{-ix}}{2} \, dx \\
&= \frac{1}{2} \frac{1}{2+i} e^{(2+i)x} + \frac{1}{2} \frac{1}{2-i} e^{(2-i) x} \\
&=\boxed{\frac{2}{5} e^{2x}\cos x + \frac{1}{5} e^{2x}\sin x + C}
\end{align}
$$

It works. We just need to know our complex numbers.

