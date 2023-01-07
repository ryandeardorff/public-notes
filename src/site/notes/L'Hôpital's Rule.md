---
{"dg-publish":true,"permalink":"/l-hopital-s-rule/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

#math 
> [[MAT 150 Hub - Calc I|MAT 150 Hub - Calc I]]

$$
\text{Let } f,g \text{ be fractions such that:} \\
$$
$$
\begin{align}
&\lim_{x\rightarrow a} f(x) = 0 &\lim_{x\rightarrow a} g(x) = 0 \\
\\
&\text{In this case} \\
&\lim_{x\rightarrow a} \frac{f(x)}{g(x)} = \lim_{x\rightarrow a} \frac{f'(x)}{g'(x)}
\end{align}
$$

This *only* works on [[Indeterminates|Indeterminates]].


---
### Discovering it:
$$
\lim_{x\rightarrow0} = \frac{\sin{x}}{x}
$$

$$
\begin{align}
\sin(x+h) &= \sin x + \cos x h + O(h^{2}) \\
\sin(0+h) &= \sin 0 + \cos 0 h = O(h^{2}) \\
&= 0 + h + O(h^{2}) \\
(x+h) &= x + h + O(h^{2}) \\
(0 + h)&= 0 + h + O(h^{2})
\end{align}
$$

going back to the top:
$$
\frac{\sin(0+h)}{0+h} = \frac{0+1h+O(h^{2})}{0+1h+O(h^{2})} = 1
$$
