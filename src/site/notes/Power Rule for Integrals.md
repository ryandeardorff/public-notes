---
{"dg-publish":true,"permalink":"/power-rule-for-integrals/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

#math 
> [[MAT 150 Hub - Calc I|MAT 150 Hub - Calc I]], [[Properties of Integrals|Properties of Integrals]]

$$
\int x^{n} dx = \frac{1}{n+1} x^{n+1} + C
$$
Where $n \ne 1$.

The $x$ term must match the [[Differentials|differential]]:
$$
\int \textcolor{orange}x^{n}\, d\textcolor{orange}x
$$

---
### Why?
$$
\begin{align}
\frac{dx^{3}}{dx} = 3x^{2} \quad &\int x^{3} dx = \frac{1}{4}x^{4}+ C\\
& \frac{d}{dx} \frac{1}{4}x^{4} = \frac{1}{4}(4x^{3}) = x^{3} \quad \textcolor{green}\checkmark
\end{align}
$$
