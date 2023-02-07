---
{"dg-publish":true,"permalink":"/lesser-of-2-evils-integration-by-parts-example/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

#math 
> [[MAT 200 Hub - Calc II|MAT 200 Hub - Calc II]], [[Integration by Parts|Integration by Parts]]

$$
\int x^{3}\ln x \,dx
$$

When we're picking the $u$ and $dv$, there's the temptation to focus on reducing the power of $x^{3}$, since normally we'd like to avoid that integral of $x^{3}$ increasing the power. But we care a lot more about taking the derivative of $\ln x$ than we do about avoiding taking the integral of $x^{3}$!

$$
\begin{align}
u=\ln x && dv = x^{3}\, dx\\
du = \frac{1}{x}\, dx  && v =  \int x^{3}dx = \frac{1}{4}x^{4}
\end{align}
$$

$$
\begin{align}
\int x^{3}\ln x \,dx &= (\ln x)\left(\frac{1}{4}x^{4}\right) - \int \frac{1}{4} x^{4}\left(\frac{1}{x}\,dx\right) \\ 
&= \frac{1}{4}x^{4}\ln x - \frac{1}{16}x^{4}+C
\end{align}
$$

---

