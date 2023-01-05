---
{"dg-publish":true,"permalink":"/quotients-in-integrals/","dgHomeLink":true,"dgPassFrontmatter":false}
---

#math 
> [[MAT 150 Hub - Calc I|MAT 150 Hub - Calc I]], [[Properties of Integrals|Properties of Integrals]]

$$
\begin{align}
&\int \frac{2x+1}{x^{2}} \ dx \\
&= \int (2x+1) x^{-2} \ dx \\
&= \int 2x x^{-2} + x^{-2} \ dx \\
&= \int 2x^{-1} \ dx + \int x^{-2} dx \\
&= 2 \int x ^{-1} \ dx + \int x ^{-2} \ dx \\
&=2 \ln |x| - \frac{1}{x} + C
\end{align}
$$

We just do our best to get rid of the quotient, and use [[Power Rule for Integrals|Power Rule for Integrals]] and such.