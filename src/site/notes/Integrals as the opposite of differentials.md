---
{"dg-publish":true,"permalink":"/integrals-as-the-opposite-of-differentials/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

#math 
> [[MAT 150 Hub - Calc I|MAT 150 Hub - Calc I]]

Recall [[The Power Rule for Derivatives|The Power Rule for Derivatives]].
And recall [[Differentials|Differentials]]

We can think about [[The Integral|The Integral]] as the opposite to [[Differentials|Differentials]]/[[The Derivative|The Derivative]], see:

$$
\begin{align}
d\left(\int dx\right) &= d(x+C) \\
dx &= d(x+C) \\
dx &= 1dx \\
dx &= dx
\end{align}
$$

$$
\begin{align}
\hline
\int du &= u+C \\
u = x^{2}+x + 1 \\
\frac{du}{dx} &= 2x+1 \\
du &=(2x+1)dx \\
\int (2x+1)dx &= \int d(x^{2}+x+1) = x^{2}+x+C \\
2\int x dx + \int 1dx &= 2(\frac{1}{2}x^{2})+x+C = x^{2}+x+C
\end{align}
$$