---
{"dg-publish":true,"permalink":"/improper-integrals-at-values-not-in-the-domain-asymptotes/","dgHomeLink":true,"dgPassFrontmatter":false}
---

#math 
> [[MAT 150 Hub - Calc I|MAT 150 Hub - Calc I]], [[Improper Integrals|Improper Integrals]]

$$
\int_{0}^{1} \frac{1}{x^{2}} dx
$$
Note that this function is *not defined at $0$*.

$$
\begin{align}
&=\lim_{a\rightarrow 0^{+}} \int_{a}^{1} \frac{1}{x^{2}} dx \\
&=\lim_{a\rightarrow 0^{+}} \frac{-1}{x} \bigg|_{a}^{1} \\
&=\lim_{a\rightarrow 0^{+}}\left(\frac{-1}{1}+ \frac{1}{a}\right) \\
&= -1 + \frac{1}{0^{+}} \\
&= \boxed{-1 + \infty} \textcolor{orange}{\leftarrow\text{diverges}}
\end{align}
$$

But it won't always diverge:
This also has an asymptote at $0$.
$$
\begin{align}
\int_{0}^{1} \frac{1}{\sqrt{x}} dx &= \int_{0}^{1} \frac{1}{x^{\frac{1}{2}}} \\
&=\int_{0}^{1} x ^{\frac{-1}{2}} dx \\
&=\lim_{a\rightarrow 0^{+}}\int_{a}^{1} x ^{\frac{-1}{2}} dx \\
&= \lim_{a\rightarrow 0^{+}} 2 x ^{\frac{1}{2}} \bigg|_{a}^{1} \\
&= \lim_{a\rightarrow 0^{+}} \left(2\cdot 1^{\frac{1}{2}} - 2 \cdot a^{\frac{1}{2}}\right) \\
&= \lim_{a\rightarrow 0^{+}} (2-2\sqrt{a}) \\
&= 2 - 2\sqrt{0} \\
&= \boxed2 \textcolor{orange}{\leftarrow\text{converges}}
\end{align}
$$