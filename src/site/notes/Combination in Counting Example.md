---
{"dg-publish":true,"permalink":"/combination-in-counting-example/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

> [[MAT 258 Hub - Discrete Mathematics|MAT 258 Hub - Discrete Mathematics]], [[Combination in Counting|Combination in Counting]]

There are 40 students in the class. In how many ways can we select a committee of 4? (each having the same role)-- unlike [[Permutations in Counting Example|Permutations in Counting Example]].

In [[Permutations in Counting Example|Permutations in Counting Example]] - A B C D, we can combine these $4!$ ways, this is the factor by which we overcount for this example-- the ordering of the jobs.

So we divide by that factor of overcounting.

\# of grounds of size $4$ out of $40$ is $\frac{40!}{\frac{36!}{4!}} = \frac{40!}{36!4!} = C(40,4) = \begin{pmatrix}40 \\ 4\end{pmatrix}$
