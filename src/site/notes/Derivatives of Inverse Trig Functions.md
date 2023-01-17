---
{"dg-publish":true,"permalink":"/derivatives-of-inverse-trig-functions/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

#math 
>[[MAT 150 Hub - Calc I|MAT 150 Hub - Calc I]]

$$
\frac{d}{dx}\arcsin{x} = \frac{1}{\sqrt{1-x^{2}}}
$$
$$
\frac{d}{dx}\arccos{x} = \frac{-1}{\sqrt{1-x^{2}}}
$$
Kinda wild they're just negatives of each other huh.
$$
\frac{d}{dx}\arctan{x} = \frac{1}{1+x^{2}}
$$

All of these also end up with no trig functions! *Just don't think about the next calculus class...*

### Theory
$$
\begin{align}
y &= \arcsin x \\
\sin (y) &= x \\
\end{align}
$$
then [[Implicit Differentiation|Implicit Differentiation]]
$$
\begin{align}
\frac{d}{dx}\sin(y)=\frac{dx}{dx} \\
\dots \\
y' = \frac{1}{\cos{y}}
\end{align}
$$
But we want our function in terms of $x$.
*The naïve way is to do $y'=\frac{1}{\cos{y}} = \frac{1}{\cos(\arcsin(x))}$, but DON'T JUST DO THIS!!!*
We can think of [[Sine Square plus Cosine Squared formula|Sine Square plus Cosine Squared formula]], 
$$\cos(\arcsin(x)) \rightarrow \sqrt{1-x^{2}}$$
So:
$$
\boxed{
\frac{d}{dx} \arcsin{x} = \frac{1}{\sqrt{1-x^{2}}}
}
$$

There's also a graphical triangular way to do this whole getting from $\cos(\arcsin(x))$ situation. Just a heads up.
