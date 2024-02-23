---
{"dg-publish":true,"permalink":"/picking-2-cards-with-conditional-probability/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

> [[MAT 258 Hub - Discrete Mathematics|MAT 258 Hub - Discrete Mathematics]]

Pick 2 cards from a deck of 52, find probability both are spades.

Method 1:
$$
P(2s) = \frac{\begin{pmatrix}13 \\ 2\end{pmatrix}}{\begin{pmatrix}52 \\ 2\end{pmatrix}} = \frac{13!}{2!11!} = \frac{13\times12}{52\times51}

$$
Method 2:
$$
P(25) = \frac{13\times12}{52\times51}
$$

Method 3:
$$
P(25) = \frac{13}{52}\times \frac{12}{51} = P(A) \cdot P(B|A)
$$
$A=$ 1st card is spade.
$B=$ 2nd card is spade.