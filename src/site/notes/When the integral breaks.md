---
{"dg-publish":true,"permalink":"/when-the-integral-breaks/","dgHomeLink":true,"dgPassFrontmatter":false}
---

#math 
> [[MAT 150 Hub|MAT 150 Hub]]

We can't solve this:
$$
\int e^{-x^{2}} dx
$$

Plugging this into something like wolfram alpha would get us:
$$
\frac{2}{\sqrt{\pi}} erf(x) +C
$$

which is... what?
$$
erf'(x) = \frac{2}{\sqrt{\pi}}e^{-x^{2}}
$$
We're walking in circles, it similar to saying, what's the value of x:
$$
x^{2}= 2
$$
Well, it's $\sqrt{2}$, right? Well what is $\sqrt{2}$?
We've invented $\sqrt{\quad}$.

In the case of $erf()$ the calculator might use [[Taylor Series|Taylor Series]] to calculate a value for this.