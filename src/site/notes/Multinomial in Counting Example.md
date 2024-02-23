---
{"dg-publish":true,"permalink":"/multinomial-in-counting-example/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

> [[MAT 258 Hub - Discrete Mathematics|MAT 258 Hub - Discrete Mathematics]]

Roll $8D6$ (8 6-sided dice)
A) # of ways to get two 2's and six 6's

total # sequences of 2's and 6's is $2^{8}$-- but we only care about ones with two 2's and such.
- **Choose** where the 2's go: $\begin{pmatrix}8\\2\end{pmatrix}$
  then 6's go in the remaining spots
  or $\begin{pmatrix}8\\2\end{pmatrix}$$\begin{pmatrix}6\\6\end{pmatrix}$


B) # of ways to get two 4's, five 3's, one 6.
- **Choose** where the 4's go: $\begin{pmatrix}8\\2\end{pmatrix}$ <-- *out of 8 spots we're choosing 2*
- Choose where the 3's go: $\begin{pmatrix}6\\5\end{pmatrix}$ <-- out of 6 remaining spots, choose 5
- Choose where $6$ goes: $\begin{pmatrix}1\\1\end{pmatrix}$
- $\begin{pmatrix}8\\2\end{pmatrix}\begin{pmatrix}6\\5\end{pmatrix}\begin{pmatrix}1\\1\end{pmatrix}$

$$
\begin{pmatrix}8\\2\end{pmatrix}\begin{pmatrix}6\\5\end{pmatrix}\begin{pmatrix}1\\1\end{pmatrix} = \frac{8!}{2!5!1!}
$$

[[Multinomial in Counting|Multinomial in Counting]]