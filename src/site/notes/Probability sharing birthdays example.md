---
{"dg-publish":true,"permalink":"/probability-sharing-birthdays-example/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

> [[MAT 258 Hub - Discrete Mathematics|MAT 258 Hub - Discrete Mathematics]]

How many people must be in a group so that the probability of at least 2 sharing a birthday is over 50%?
(use 366 days for a year)

a) Let $E:$ at least 2 out of a total of $N$ people share a birthday.

Solve for $N$ so that $P(E)>0.5$

b) Find smallest $N$ so that $P(E)=1$
N=367 by [[Pigeonhole Principle|Pigeonhole Principle]].

Back to (a): easier to find $P(E^{C})$

$$
\begin{align*}
E^{C} &=  N \text{ people have } N \text{ distinct birthdays}\\
P(E^{C}) &= \frac{366\times365\times364\times\dots\times(366-N+1)}{366^{N}}
\end{align*}
$$

Since $P(E)>0.5$
$1-P(E^{C})>0.5$
$P(E^{C})<0.5$
$$\frac{\frac{366!}{366-N!}}{366^{N}} < 0.5$$

*Then we try N values (divide an conquer style) until we get an answer...*
$N=22 \rightarrow P(E^{C )}= 0.5252$
$\boxed{N=23} \rightarrow P(E^{C}) = 0.4936$