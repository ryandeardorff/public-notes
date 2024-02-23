---
{"dg-publish":true,"permalink":"/drawing-cards-independence-example-probability/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

> [[MAT 258 Hub - Discrete Mathematics|MAT 258 Hub - Discrete Mathematics]], [[Independence (Probability)|Independence (Probability)]], [[Overlap and Unions in Sets (Probability) notation|Overlap and Unions in Sets (Probability) notation]]

Draw 2 cards from 52. (w/o replacement)
$B =$ second card is spade.
Are $A$ and $B$ [[Independence (Probability)|independent]]?

a) $A=$ the first card is Ace
$P(A) = \frac{4}{52} = \frac{1}{13}$
$P(B) = \frac{13\times 12 + 39 \times 13}{52\times 51}$ <-- the $13\times 12$ is for choosing a spade followed by spade, then the $39\times13$ is non-spade followed by spade.
$=\frac{1}{4}$
$P(A\cap B)= \frac{1\times12 + 3\times13}{52\times51}$ (ace of spades follow by spade + ace of non-spade follow by spade)
$=\frac{1}{52}$

$\frac{1}{52}=\frac{1}{13}+ \frac{1}{4}$
$A,B$ are [[Independence (Probability)|Independent]].



b) $A=$ first card is spade
$P(A)=\frac{1}{4}$
$P(B)=\frac{1}{4}$ (we already found this)
$P(A\cap B) = \frac{13\times12}{52\times51} = \frac{3}{51} = \frac{1}{17}$
$\frac{1}{17}\ne \frac{1}{4}\times \frac{1}{4}$

Q: 52 cards, pick one at a time:
$P(1^{st}\text{is spade}) = \frac{1}{4}$
$P(2^{nd}\text{ is spade}) = \frac{1}{4}$
$P(11^{th}\text{ is a spade}) = \frac{1}{4}$
$P(52^{nd} \text{ is a spade}) = \frac{1}{4}$

notice that they're all $\frac{1}{4}$ nothing about the 11th or 52nd is special.