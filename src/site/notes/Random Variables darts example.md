---
{"dg-publish":true,"permalink":"/random-variables-darts-example/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

> [[MAT 258 Hub - Discrete Mathematics|MAT 258 Hub - Discrete Mathematics]]

Play darts until 1st hit of target. The probability I hit the target in one play is 0.2. 
Let $X=$ \# of plays until 1st hit.
$P(x=4)=(0.8)\cdot(0.8)\cdot(0.8)\cdot(0.2)$
$P(x=k)=(0.8)^{k-1}\cdot(0.2)\quad1\le k\lt \infty$

$$
\begin{align*}
E[x] &=  \sum\limits_{\text{all } k} k P(x=k)\\
&= \sum\limits_{k=1}^{\infty} k\cdot (0.8)^{k-1}(0.2)&\leftarrow \text{calculator on this}\\
&= \frac{1}{0.2}\\
&= 5
\end{align*}
$$
$X= \text{Geometric}(0.2)$
Check:
$$
\sum\limits_{k=1}^{\infty} P(x=k)=1
$$
$$
\begin{align*}
&\sum\limits_{k=1}^{\infty}(0.8)^{k-1}(0.2)\\
&= (0.2) \sum\limits_{j=0,\,j=k-1}^{\infty}(0.8)^{j}\\
&= (0.2) \frac{1}{1-0.8} = 1\\

\end{align*}
$$
*We used [[Geometric Series|Geometric Series]] to compute this one*
