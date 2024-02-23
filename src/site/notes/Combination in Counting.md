---
{"dg-publish":true,"permalink":"/combination-in-counting/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

> [[MAT 258 Hub - Discrete Mathematics|MAT 258 Hub - Discrete Mathematics]], [[Combination in Counting Example|Combination in Counting Example]]

$$
\begin{pmatrix}n \\ k\end{pmatrix} = C(n,k) = \frac{n!}{k!(n-k)! }
$$
... a combination of $n$ objects taken $k$ at a time is the number of **unordered** subsets of size $k$ out of $n$ objects.

Seems like it reads as $n$ choose $k$ (?)

Remarks:
1) 
$$
\begin{pmatrix}n \\ k\end{pmatrix} = \begin{pmatrix}n \\ n-k\end{pmatrix} = \frac{n!}{k!(n-k)!}
$$
$$
\begin{pmatrix}n \\ 0\end{pmatrix} = \begin{pmatrix}n \\ n\end{pmatrix} = 1
$$
$$
\begin{pmatrix}n \\ 1\end{pmatrix} = \begin{pmatrix}n \\ n-1\end{pmatrix} = n
$$
2) Interpret $C(n,k)$ as $n$ "choose" $k$