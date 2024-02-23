---
{"dg-publish":true,"permalink":"/binomial-random-variables/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

> [[MAT 258 Hub - Discrete Mathematics|MAT 258 Hub - Discrete Mathematics]]

Roll 4D6. Let $X=\#6's$
$P(x=0)=(\frac{5}{6})^{4}$
$P(x=1)=\left(\frac{1}{6}\right)\cdot\left(\frac{5}{6}\right)^{3}\cdot\begin{pmatrix}4 \\ 1\end{pmatrix}$
$P(x=2)=\left(\frac{1}{6}\right)^{2}\cdot\left(\frac{5}{6}\right)^{2}\cdot\begin{pmatrix}4 \\ 2\end{pmatrix}$
$P(x=3)=\left(\frac{1}{6}\right)^{3}\cdot\left(\frac{5}{6}\right)\cdot\begin{pmatrix}4 \\ 3\end{pmatrix}$
$P(x=4)=\left(\frac{1}{6}\right)^{4}$

This is a binomial random variable.
$X=\text{Binomial}(4,\frac{1}{6})$

If $X=Bionmial(n,p)$ where $n=\#\text{trials}$, $p=\text{prob. of success}$.
$E[x]=np$ and $P(x=k)=\begin{pmatrix}n \\ k\end{pmatrix}p^{k}(1-p)^{n-k}, 0\le k \le n$
In this example, the average \# of 6's in rolling 4D6 is $4\left(\frac{1}{6}\right)= \frac{2}{3}$

Check:
$$
\sum\limits_{k=0}^{n}\begin{pmatrix}n \\ k\end{pmatrix}p^{k}(1-p)^{n-k} = 1
$$
true from [[Binomial Theorem|Binomial Theorem]]
with $x=p$
and $y=1-p$
sum = $(p+(1-p))^{n}=1$
