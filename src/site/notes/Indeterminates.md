---
{"dg-publish":true,"permalink":"/indeterminates/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

#math 
> [[MAT 150 Hub - Calc I|MAT 150 Hub - Calc I]]

$$
\frac{0^{+}}{0^{+}}
$$
is an example of an indeterminate, which means that the value depends on *speeds*, how fast do each of these approach $0$?

---
##### Types of Indeterminates:
$$
\begin{align}
\infty-\infty &&\frac{0^{+}}{0^{+}}&& \frac{\infty}{\infty} 
 && 0^{+}\infty
\end{align}
$$
###### There's more though, involving powers
$$
\begin{align}
(0^{+})^{0^{+}} & & \infty^{0^{+}} & & (1^{+})^{\infty}
\end{align}
$$

^7b52ed

---
##### Getting There:
$$
\lim_{x\rightarrow 0} \frac{\sin{x}}{x} = \frac{\sin0}{0}
$$
We could try [[Trending Values in Limits|Trending Values in Limits]], but:
$$
\lim_{x\rightarrow 0^{+}} = \frac{\sin{0^{+}}}{0^{+}} = \frac{0^{+}}{0^{+}}
$$
This is still the same problem with [[More Examples of Trending Values#^5fd1ec|More Examples of Trending Values#^5fd1ec]].