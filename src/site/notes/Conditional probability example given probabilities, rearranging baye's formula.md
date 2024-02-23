---
{"dg-publish":true,"permalink":"/conditional-probability-example-given-probabilities-rearranging-baye-s-formula/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

> [[MAT 258 Hub - Discrete Mathematics|MAT 258 Hub - Discrete Mathematics]]

Given 2 events $A$ and $B$ with $P(A) = 0.2$, $P(B) = 0.3$ and $P(A|B) = 0.5$, find:
a) $P(A\cap B)$
b) $P(B|A)$

a)
We're using [[Baye's Formula|Baye's Formula]], in which we divide by $B$, so here we'll multiply by $P(B)$ (we rearranged the formula).
$P(A\cap B) = P(A|B)P(B) = (0.5)(0.3) = 0.15$

b)
$P(B|A) = \frac{P(A\cap B)}{P(A)} = \frac{0.15}{0.2}=0.75$