---
{"dg-publish":true,"permalink":"/diverging-improper-integrals/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

#math 
> [[MAT 150 Hub - Calc I|MAT 150 Hub - Calc I]], [[Improper Integrals|Improper Integrals]]

$$
\begin{align}
\int_{0}^{\infty} e^{x}dx &=\lim_{b\rightarrow\infty} \int_{0}^{b} e^{x}dx \\
&= \lim_{b\rightarrow\infty} e^{x}\bigg|_{0}^{b} \\
&= \lim_{b\rightarrow\infty}(e^{b} - 1)\\ 
&= e^{\infty} - 1  \\
&= \boxed\infty \textcolor{orange}{\leftarrow \text{diverges}}
\end{align}
$$
