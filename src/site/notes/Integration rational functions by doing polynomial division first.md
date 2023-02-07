---
{"dg-publish":true,"permalink":"/integration-rational-functions-by-doing-polynomial-division-first/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

#math 
> [[MAT 200 Hub - Calc II|MAT 200 Hub - Calc II]]

If we do a [[u-substitution (integrals)|u-substitution (integrals)]] with the denominator of:
$$
\int \frac{x^{2}-x+4}{x-3} \, dx
$$
We will find we get:
$$
\int(u+5+10 u^{-1})\, du
$$
Which is totally doable-- we can solve it.

But we have an **alternate way** now:

$$
\int \frac{x^{2}-x+4}{x-3} \, dx
$$
1. Look at the [[Degree of a rational function|degree of the rational function]]. We will get $1$.
	1. If that # $\ge0$, we should try using [[Polynomial Division|Polynomial Division]]
	2. In this case that would get us: $$\int\left(x+2+ \frac{10}{x-3}\right)\, dx$$

That makes our lives a lot easier!