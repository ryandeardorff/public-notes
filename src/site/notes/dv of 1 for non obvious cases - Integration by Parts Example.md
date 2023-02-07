---
{"dg-publish":true,"permalink":"/dv-of-1-for-non-obvious-cases-integration-by-parts-example/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

#math 
> [[MAT 200 Hub - Calc II|MAT 200 Hub - Calc II]], [[Integration by Parts|Integration by Parts]]

$$
\int \ln x \,dx
$$

First, it's $\color{red}\ne \frac{1}{x}+C$

$$
\begin{align}
u=\ln x && dv= dx\\
du = \frac{1}{x}\,dx && v=\int1\,dx = x \\
\end{align}
$$
Woah. That's better.
$$
\begin{align}
&= (\ln x)x - \int x\left(\frac{1}{x}dx\right)\\
&= x\ln x - \int 1 \,dx \\
&= \boxed{x\ln x - x + C}
\end{align}
$$
