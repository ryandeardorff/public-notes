---
{"dg-publish":true,"permalink":"/examples-of-trig-substitution/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

#math 
> [[MAT 200 Hub - Calc II|MAT 200 Hub - Calc II]], [[Intro to Trigonometric Substitution (Trig functions appearing in non-trig integrals)|Intro to Trigonometric Substitution (Trig functions appearing in non-trig integrals)]], [[When to use Trig Substitution|When to use Trig Substitution]]

### 1
$$
\begin{align}
&\int \frac{x^{2}}{(1-x^{2})^{\frac{3}{2}}} \, dx \\ \\
&\int x^{2} (1-x^{2})^{\frac{-3}{2}}\, dx \\ \\
&\int \frac{x^{2}}{(\sqrt{1-x^{2}})^{3}} \, dx
\end{align}
$$

```ad-check
title: Solution
collapse:

$$
\begin{align}
&x = \sin\theta \\
&dx = \cos\theta \, d\theta \\ \\
&= \int \frac{x^{2}}{(1-x^{2})^{\frac{3}{2}}} \cos\theta \, d\theta \\
&= \int \frac{\sin^{2}\theta}{(1-\sin^{2}\theta)^{\frac{3}{2}}} \cos\theta \, d\theta \\
&= \int \frac{\sin^{2}\theta}{(\cos^{2}\theta)^{\frac{3}{2}}} \cos \theta \, d\theta \\
&= \int \frac{\sin^{2}\theta}{\cos^{2}\theta} \, d\theta \\
&= \int \tan^{2}\theta \, d\theta \\
\end{align}
$$

Huh. We should be able to do that, see:[[Integrals of Trig Functions#^fa45d5]]! (opposite of [[Derivative of Tangent]])

$$
\begin{align}
&= \int (\sec^{2}\theta - 1) \, d \theta \\
&= \tan\theta - \theta + C \\
\color{gray}
x=\sin\theta \\
\theta = \arcsin x \\ 
&= \boxed{\frac{x}{\sqrt{1-x^{2}}} - \arcsin(x) + C}
\end{align}
$$

```

### 2
$$
\int \frac{1}{1+2x^{2}} \, dx
$$

```ad-check
title: Solution
collapse:
We want to use the identity [[Tangent squared + 1]]:

$1+ \tan^{2}\theta = \sec^{2}\theta$

which will get us the substitution:

$x= \frac{1}{\sqrt{2}} \tan\theta$

After a bunch of algebra:
$$
\begin{align}
&\frac{1}{\sqrt2} \int \, d\theta\\
&= \frac{1}{\sqrt2}\theta + C \\
&= \boxed{\frac{1}{\sqrt2}\arctan\sqrt2 x + C}
\end{align}
$$

```