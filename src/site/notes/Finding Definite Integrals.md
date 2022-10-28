---
{"dg-publish":true,"permalink":"/finding-definite-integrals/","dgHomeLink":true,"dgPassFrontmatter":false}
---

#math 
> [[MAT 150 Hub|MAT 150 Hub]], [[The Integral|The Integral]]

$$
\int_{a}^{b} f(x) \ dx = F(b) - F(a)
$$

Which means we do [[The Integral|indefinite integrals]] first:
$$
\begin{align}
&F(x) + C = \int f(x) \ dx \\ \\
&\text{plug in a and b:} \\
&F(b) - F(a)
\end{align}
$$
That indefinite integral basically gets us a "Running total function".

So when we want to look at a range, we just find the running total from the whole curve up to the value ($F(b)$) then removing the stuff before the range ($F(a)$).

This also still works with negative range values for $a$ or $b$.