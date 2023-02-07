---
{"dg-publish":true,"permalink":"/partial-fractions/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

#math 
> [[MAT 200 Hub - Calc II|MAT 200 Hub - Calc II]]

It's the process of un-simplifying a complex denominator, using essentially the reverse of common denominators.

$$
\frac{1}{x-1} - \frac{1}{x+1} = \frac{(x+1)-(x-1)}{(x-1)(x+1)} = \frac{2}{x^{2}-1}
$$

We can go backwards through this process!!!

$$
\int \frac{1}{(x-1)(x+1)} \, dx = \frac{1}{2}\int \frac{2}{x^{2}-1} = \frac{1}{2} \int \frac{1}{x-1} - \frac{1}{x+1} \, dx
$$

Look at that! We can solve that!