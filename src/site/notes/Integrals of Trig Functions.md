---
{"dg-publish":true,"permalink":"/integrals-of-trig-functions/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

#math 
> [[MAT 200 Hub - Calc II|MAT 200 Hub - Calc II]]

[[Integral of Sine|Integral of Sine]]

---
[[Integral of Cosine|Integral of Cosine]]

---
$$
\int \sec^{2}\theta \, d\theta = \tan\theta + C
$$
From [[Derivative of Tangent|Derivative of Tangent]]

---

$$
\tan^{2}\theta \, d \theta = \int (\sec^{2}\theta - 1)\,  d \theta = \int sec^{2}\theta \, d\theta - \int\, d\theta = \boxed{\tan\theta - \theta + C}
$$

---
$$
\int\sec\theta \, d\theta = \int\sqrt{1+\tan^{2}\theta} \, d\theta = ?
$$

---

# Some more complicated problems:

```ad-question
title: Problem
$$
\int \sin\theta \cos\theta \, d\theta
$$
```

```ad-check
title:Solution  🕶
collapse:
$$
\begin{align}
\int \sin\theta \cos\theta \, d\theta &= \\
u=\cos\theta \\
\frac{du}{d\theta} = -\sin\theta \\
du = -\sin\theta d \theta \\
d\theta = \frac{1}{-\sin\theta} du \\
&= \int\sin\theta\cos\theta \frac{1}{(-1)\sin\theta} \, du \\
&= -\int \cos\theta \, du \\
&= -\int u\, du\\
&= \frac{-1}{2} u^{2}+ C\\
&=\boxed{\frac{-1}{2} \cos^{2}\theta + C}
\end{align}
$$

We could also still end up with $\boxed{\frac{1}{2}\sin^{2}\theta + C}$ if we use $u=\sin\theta$
Which is actually equivalent!
$$
\frac{-1}{2}\cos^{2}\theta + C \quad \rightarrow\quad  \frac{-1}{2}(1-\sin^{2}\theta) + C \quad \rightarrow\quad  \frac{1}{2}+ \frac{1}{2}\sin^{2}\theta + C
$$
See it?
```

```ad-question
title:Problem
$$
\int \sin\theta \cos^{2}\theta \, d\theta
$$
```

```ad-check
title: Solution
collapse:
$$
\begin{align}
\int\sin\theta \cos^{2}\theta \, d\theta &= \\
u = \cos\theta \\
\frac{du}{d\theta} = -\sin\theta \\
d\theta = \frac{1}{-\sin\theta}du\\
&=\int\sin\theta\cos^{2}\theta \frac{1}{(-1)\sin\theta}\, du\\
&=-\int u^{2} \, du\\
&=\boxed{\frac{-1}{3} (\cos\theta)^{3} + C}
\end{align}
$$
```