---
{"dg-publish":true,"permalink":"/trickier-trig-integrals-solving-even-powered-trig-integrals-using-double-angles/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

#math 
> [[MAT 200 Hub - Calc II|MAT 200 Hub - Calc II]] ,[[Integrals of Trig Functions|Integrals of Trig Functions]], [[Double Angle Formulas|Double Angle Formulas]]

$$
\int \sin^{2}\theta \, d\theta
$$
It's an even power... Uh oh.

# The problem with it:
We could try our usual [[u-substitution (integrals)|u-substitution (integrals)]] tricks, but it's not great:
$$
\begin{align}
u=\sin\theta \\
\frac{du}{dx} = \cos\theta \\
\dots \\
\textit{We'll end up with:} \\
\int \frac{u^{2}}{\sqrt{1-u^{2}}} \, du
\end{align}
$$
Which is not great...
So... 👀

# Solution:
We're gonna need to use some [[Double Angle Formulas|Double Angle Formulas]] (in particular in this case the $\cos{2\theta}$ one).
*Remember, [[The Integral|integrals]] often involve this idea of "unsimplifying"-- getting to a less simple form, that takes us somewhere useful.*
$$
\int \sin^{2}\theta \, d\theta
$$

$$
\begin{align}
&= \int \frac{1-\cos(2\theta)}{2} \, d\theta \\
&= \int \frac{1}{2} - \frac{\cos2\theta}{2} \, d\theta \\
&= \int \frac{1}{2} \, d\theta - \frac{1}{2} \int \cos(2\theta) \, d\theta \\
&= \frac{1}{2} \theta - \frac{1}{2}\int\cos(2\theta) \, d\theta \\ \\
&\color{gray}\text{a u-sub will work great here :)} \\
&\quad u=2\theta\\
&\quad \frac{du}{dx} = 2 \\
&\quad d\theta = \frac{1}{2} du \\ \\

&= \frac{1}{2}\theta - \frac{1}{4} \int \cos(u) \, du \\
&= \frac{1}{2}\theta - \frac{1}{4} \sin(u) + C \\
&= \boxed{\frac{1}{2}\theta - \frac{1}{4} \sin(2\theta) + C}
\end{align}
$$

We could also recognize the [[Double Angle Formulas|double angle]] in that answer and rewrite it, but that's not necessarily better or worse.