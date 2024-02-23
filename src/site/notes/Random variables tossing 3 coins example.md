---
{"dg-publish":true,"permalink":"/random-variables-tossing-3-coins-example/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

> [[MAT 258 Hub - Discrete Mathematics|MAT 258 Hub - Discrete Mathematics]], [[Random Variables|Random Variables]]

Toss 3 coins. Let $x=$ # of heads.

a) find the probability mass function (pmf) of x.
b) Find $E[x]$ (the weighted average).

a)
$x\in\set{0,1,2,3}$
$P(x=0) = \frac{1}{8}$ (all T)
$P(x=1) = \frac{3}{8}$ (HTT,THT,TTH)
$P(x=2)=\frac{3}{8}$
$P(x=3) = \frac{1}{8}$
$---------$
Adds to 1? ✔

b)
$$\begin{align*}
E[x] &= 0\cdot P(x=0) + 1\cdot P(x=1) + 2\cdot P(x=2) + 3\cdot P(x=3)\\
&= 0\cdot \frac{1}{8} + 1\cdot \frac{3}{8} + 2\cdot \frac{3}{8} + 3\cdot \frac{1}{8}\\
&= \frac{12}{8}\\
&= 1.5
\end{align*}$$