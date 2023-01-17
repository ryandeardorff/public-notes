---
{"dg-publish":true,"permalink":"/tangent-substitution-for-solving-trig-integrals/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

#math 
> [[MAT 200 Hub - Calc II|MAT 200 Hub - Calc II]]

# The Procedure
$$
\int (\sin\theta)^{m}(\cos\theta)^{n} \, d\theta
$$
If $m+n$ is even, and negative, use $u=\tan\theta$

**NOTE: This won't be on the [[MAT 200 Hub - Calc II|MAT 200 Hub - Calc II]] test, since it's just so obtuse.** (which also happens to be an unintentional angle pun)

# Finding It
$$
\begin{align}
&\int \frac{1}{\sin\theta\cos\theta} \, d \theta \\ \\

u= \tan\theta \\
du = \sec^{2}\theta \, d\theta \\
\frac{du}{d\theta} = \sec^{2}\theta \\
d\theta = \cos^{2}\theta du \\

&=\int \frac{\cos^{2}\theta}{\sin\theta\cos\theta} \,du \\
&= \int \frac{\cos\theta}{\sin\theta} \, du \\
&= \int \frac{1}{u} \, du \\
&= \boxed{\ln|\tan\theta| + C}
\end{align}
$$

