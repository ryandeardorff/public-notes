---
{"dg-publish":true,"permalink":"/proving-existence-theorems/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

#math 
> [[MAT 258 Hub - Discrete Mathematics|MAT 258 Hub - Discrete Mathematics]]

To prove existence theorems, we can use
1. [[Constructive Proof Example for Circles and Equilateral Triangles|Constructive Proof]]
2. Existence Proof. [[Theorem for Existence and Forall|Theorem for Existence and Forall]]?

### Ex. 1
There exists some integer that is both a perfect square and a perfect cube
That is, there is some $n$ so that 
$n=k^{2}$, with  $k\in\mathbb{Z}$ and
$n=l^{3}$ with $l\in\mathbb{Z}$

Proof: construct an example.
$1=1^{2}$
$1=1^{3}$
$1$ proves the theorem.
Other choices: 0, 64 ($64=8^{2},\, 64=4^{3}$)
### Ex. 2
I have 16 markers. They come in 3 colors. There is at least one color with 6 or more markers.

Proof (existence proof):
[[Proof by Contradiction|Proof by Contradiction]]...
Suppose this is not true it is not the case that there is at least one color with 6 or more markers. So no color has 6 or more markers which means each color has less than 6 markers.
So each color can have at most 5 markers.
In total there are at most $5*3=15$ markers. <---- contradiction!
This contradicts that we have $16$ markers, so we conclude that at least one color has more than 5 markers.