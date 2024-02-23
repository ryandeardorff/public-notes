---
{"dg-publish":true,"permalink":"/proof-by-contradiction/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

#math 
> [[MAT 258 Hub - Discrete Mathematics|MAT 258 Hub - Discrete Mathematics]], [[Types of Proofs|Types of Proofs]]

Show $p\rightarrow q$ by showing $p\land \neg\,q$ is false.
*Recall $(p\rightarrow q) \equiv (\neg\,p\lor q)\equiv \neg(p\land\neg\,q)$ <-- definition of implication*

### Ex: 
Theorem: (If axioms of $\mathbb{R}$ hold, then) $\sqrt{2}$ is irrational. *<-- the ( ) section is implied, we assume that all real number stuff holds.*

Def: 
<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">

<div class="markdown-embed-title">



</div>


#math 
> [[MAT 258 Hub - Discrete Mathematics|MAT 258 Hub - Discrete Mathematics]]

A rational number is a real number that can be expressed as $\frac{a}{b}$ with $a,b\in\mathbb{Z},\, b\ne0$
$\mathbb{Q} =$ set of rationals = $\set{\frac{a}{b}|a,b\in\mathbb{Z}, b\ne 0}$
An irrational number cannot be written as above.
The set of irrationals = $\mathbb{R}-\mathbb{Q}$

</div></div>

Proof: Suppose $\sqrt{2}$ is rational.
$p$ = axioms of $\mathbb{R}$ hold.
$q$ = $\sqrt{2}$ is irrational.
$\neg\,q$ = $\sqrt{2}$ is rational.

- Then there are $a,b\in\mathbb{Z}$ with $b\ne 0$
  So that $\sqrt{2} = \frac{a}{b}$ in simplest form. (that is $a$ and $b$ have no common factors)
- Then $b\sqrt{2} = a$, $2b^{2}=a^{2}$
- This means $a^{2}$ is even, so $a$ must be even too.
- So there is some integer $k$ so that $a=2k$
- Since $2b^{2}=a^{2}$ and $a=2k$, we get $2b^{2}=(2k)^{2}$
  $b^{2}=2k^{2}$
- Then $b^{2}$ is even, which means $b$ is even.
- So there is some integer $m$ so that $\boxed{b=2m}$. <-- *This is where we get the contradiction!!!*
- Then $a$ and $b$ both have 2 as a factor, which **contradicts** that $\frac{a}{b}$ was in simplest form.
- Conclude $\sqrt{2}$ is not rational.