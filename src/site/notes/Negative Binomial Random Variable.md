---
{"dg-publish":true,"permalink":"/negative-binomial-random-variable/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

> [[MAT 258 Hub - Discrete Mathematics|MAT 258 Hub - Discrete Mathematics]]

Prob. of hitting target in a match is $0.2$
Let $x=\# \text{ matches until the }3^{rd}\text{ win}$
Find $P(x=20)=\begin{pmatrix}19 \\ 2\end{pmatrix}(0.2)^{2}(0.8)^{17}(0.2)$
$\uparrow$ 20th is a win

first 19 matches: 2 wins, 17 losses

$P(x=20)=\begin{pmatrix}19 \\ 2\end{pmatrix}(0.2)^{3}(0.8)^{17}$

In General, if $X=\text{Negative Binomial}(r,p)$
$X= \# \text{matches until }r^{\text{th}} \text{ win with prob. of success in a match being }p$
$$
P(x=k) = \begin{pmatrix}k-1  \\ r-1 \end{pmatrix} p^{r}(1-p)^{k-r}\quad r\le k \lt \infty
$$