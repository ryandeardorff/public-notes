---
{"dg-publish":true,"permalink":"/solving-squares-in-partial-fraction-denominators/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

#math 
> [[MAT 200 Hub - Calc II|MAT 200 Hub - Calc II]], [[Partial Fractions|Partial Fractions]], [[Methods of Partial Fraction Decomposition|Methods of Partial Fraction Decomposition]]

$$
\int \frac{2x+1}{(x-3)^{2}} \, dx
$$

$$
\begin{align*}
\frac{2x+1}{(x-3)(x-3)} &\ne \frac{A}{x-3}+ \frac{B}{x-3}
\end{align*}
$$

We can't use usual [[Methods of Partial Fraction Decomposition|Methods of Partial Fraction Decomposition]]. Instead:

## Method 1
This is what a lot of guides will use.
$$
\begin{align*}
\frac{2x+1}{(x-3)^{2}} &= \frac{A}{x-3} + \frac{B}{(x-3)^{2}}\\
&= \frac{Ax-3}{(x-3)^{2}} + \frac{B}{(x-3)^{2}}\\
&= \frac{Ax+B-3A}{(x-3)^{2}}
\end{align*}
$$

## Method 2
We can actually do polynomial division here!
We'll use only one power
$$
\begin{align*}
2\\
x-3 \,\overline{\smash{)}2x+1}\\
2x-6\\
\overline{\qquad 7}
\end{align*}
$$
$$
\begin{align*}
\frac{2x+1}{x-3} &= 2+\frac{7}{x-3}\\
\frac{2x+1}{(x-3)^{2}} &= \frac{2}{x-3}+ \frac{7}{(x-3)^{2}}
\end{align*}
$$

## Method 3
We could use a [[u-substitution (integrals)|u-substitution (integrals)]]!
$u=x-3, x=u+3$; $du=dx$

$$
\begin{align*}
\int \frac{2x+1}{(x-3)^{2}} \, dx &= \int \frac{2(u+3)+1}{u^{2}} \, du\\
&= \int \frac{2u+7}{u^{2}}\, du\\
&= \int \frac{2}{u}+ \frac{7}{u^{2}} \, du
\end{align*}
$$