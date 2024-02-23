---
{"dg-publish":true,"permalink":"/multinomial-in-counting/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

> [[MAT 258 Hub - Discrete Mathematics|MAT 258 Hub - Discrete Mathematics]], [[Multinomial in Counting Example|Multinomial in Counting Example]], [[Combination in Counting|Combination in Counting]]

$$
\text{The multinomial }\begin{pmatrix}n \\ n_{1},n_{2},\dots,n_{k}\end{pmatrix} = \frac{n!}{n_{1}!n_{2}!\dots n_{k}!}
$$
is the number of ways to place $n$ objects into $k$ bins of sizes $n_{1}, n_{2}, \dots, n_{k}$ with $n_{1}+n_{2}+\dots+n_{k}=n$

Remarks:
1) $$\begin{pmatrix}n \\ n_{1},n_{2},\dots,n_{k}\end{pmatrix} = \begin{pmatrix}n \\ n_{!}\end{pmatrix}\times\begin{pmatrix}n-n_{1} \\ n_{2}\end{pmatrix}\times\dots\times\overset{n_{k}}{\begin{pmatrix}n-n_{1}-n_{2}-\dots-n_{k-1} \\ n_{k}\end{pmatrix}}$$
2) $$\begin{pmatrix}n \\ n_{1},n_{2}\end{pmatrix}= \frac{n!}{n_{1}!n_{2}!} = \begin{pmatrix}n \\ n_{1}\end{pmatrix}=\begin{pmatrix}n \\ n_{2}\end{pmatrix} \quad\text{b/c}\quad n_{1}+n_{2}=n$$ Binomial
3) $$\overset{\text{ordered set of }x}{P(n,k)} = \overset{\text{unordered set of }k}{C(n,k)}\times \overset{\text{\# orderings of }k \text{ objects}}{k!}$$

