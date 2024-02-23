---
{"dg-publish":true,"permalink":"/true-of-false-with-2-input-predicates-order-of-quantifiers-matters/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

> [[MAT 258 Hub - Discrete Mathematics|MAT 258 Hub - Discrete Mathematics]], [[Predicates|Predicates]]

Decide if T/F:

Let $P(x,y)$ be $x+y^{2} = 0$, $x,y\in\mathbb{R}$

1) $\forall x\forall y \, P(x,y)$
	   F (counterexample: $x=1,y=1$)
2) $\exists x\, \exists y \, P(x,y)$
	   $P(0,0)$ is T
3) $\exists x \,\forall y\,P(x,y)$
	   F
	   For all $x$; $x+y^{2}=0$ is not T for all $y$
	   Case 1: If $x=0$ $y=1$ give $P(0,1)$ F
	   Case 2: If $x\ne 0$, $y=0$ give $P(x,0)$ F
4) $\forall y\,\exists x \,P(x,y)$
	   For every $y$, I can find an $x$ so that $x+y^{2}=0$
	   This is True! just solve for it: Let $x=-y^{2}$
	   $P(-y^{2},y)$ is T
5) $\forall x \exists y \, P(x,y)$
	   For **every** $x$, I can find $y$ so that $x+y^{2}=0$
	   Let $y=\sqrt{-x}$, but then no solution for $x\gt0$
	   *Which means it doesn't work for positive $x$*

Note: the order of quantifiers matters!