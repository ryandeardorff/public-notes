---
{"dg-publish":true,"permalink":"/options-for-doing-either-a-trig-sub-or-a-substitution-getting-more-polynomials/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

#math 
> [[MAT 200 Hub - Calc II|MAT 200 Hub - Calc II]]

$$
\int \frac{bx+c}{(x+2)^{2}+1} \, dx
$$

We could do:
$$
\begin{align}
\int \frac{b(-a+\tan\theta)+c}{\sec^{2}\theta} \sec^{2}\theta\,d\theta \\
&=-ba\theta-b\ln|\cos\theta| + c\theta
\end{align}
$$

OR **this**:
$$
\begin{align}
\int \frac{b(x+a)-ab+c}{(x+a)^{2}+1} \\
&=\int \frac{b(x+a)}{(x+a)^{2}+1}\, dx + \int \frac{-ab+c}{(x+a)^{2}+1}\, dx
\end{align}
$$
using a $w$ sub where $w=x+a$