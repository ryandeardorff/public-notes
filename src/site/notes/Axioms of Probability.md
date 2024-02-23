---
{"dg-publish":true,"permalink":"/axioms-of-probability/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

> [[MAT 258 Hub - Discrete Mathematics|MAT 258 Hub - Discrete Mathematics]]

Def: A probability measure is a function $P:\Omega\rightarrow[0,1]$
so that the following axioms hold:
1) $P(\Omega)=1$ ^06b86d
2) For any event $E$, $0\le P(E)\le 1$
3) If $E$ and $F$ are [[Event (Probability)|events]] so that $E\cap F = \emptyset$ (no overlap)
   Then $P(E\cup F) = P(E)+P(F)$ ^ebd440
4) If $E_{1},E_{2},E_{3},\dots$ are events so taht $E_{i}\cap E_{j} = \emptyset$ if $i+j$ then $P(E_{1}\cup E_{2}\cup\dots)=P(E_{1})+P(E_{2})+\dots$