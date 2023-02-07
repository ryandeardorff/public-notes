---
{"dg-publish":true,"permalink":"/method-of-undetermined-coefficients/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

#math 
> [[MAT 200 Hub - Calc II|MAT 200 Hub - Calc II]]

$$
x-3=\textcolor{orange}Ax+\textcolor{orange}A+\textcolor{orange}Bx-2\textcolor{orange}B = \underline{(\textcolor{orange}A+\textcolor{orange}B)x +(\textcolor{orange}A-2\textcolor{orange}B)}
$$
$$
\begin{align}
A+B = 1 \\
A-2B = -3
\end{align}
$$

---

If we know some part of what we expect an integral to be, such as:
$$
\int \ln x \, dx = A x\ln x + Bx + C
$$
Then we can work backwards with a derivative:
$$
\frac{d}{dx} (Ax\ln x + Bx)
$$
And find out what remains afterward, in order to figure out the amounts.
$$
= A\ln x + A+B
$$
*We want these to match what was in the integral:*
$$
A=1 \textcolor{gray} {\quad\cdot(\ln x)} \qquad A+B = 0
$$