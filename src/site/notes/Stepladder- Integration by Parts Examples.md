---
{"dg-publish":true,"permalink":"/stepladder-integration-by-parts-examples/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

#math 
> [[MAT 200 Hub - Calc II|MAT 200 Hub - Calc II]], [[Integration by Parts|Integration by Parts]]

[[Integration by Parts|Integration by Parts]] can go both ways, it can either get you simpler or harder-- and we can see a pattern from that:

First if we choose our $u$ and $dv$ well.
$$
\begin{align}
\int x \cos x \, dx
\end{align}
$$

$$
\begin{align}
u=x && dv = \cos x \, dx \\
du = 1\,dx && v = \textcolor{gray}{\int \cos x \, dx =} \sin x
\end{align}
$$

$$
\begin{align}
&= x\sin x - \int \sin x \,dx \\
&= x\sin x -(-\cos x) + C \\
&= \boxed{x\sin x + \cos x + C}
\end{align}
$$

But what if we chose poorly with $u$ and $dv$?
$$
\begin{align}
u=\cos x  && dv = x\,dx \\
\dots \\
\end{align}
$$

$$
\begin{align}
&= (\cos x)\left(\frac{1}{2} x^{2}\right)- \int \frac{1}{2} x^{2}(-\sin x) dx \\
&= \frac{1}{2}x^{2}\cos x + \frac{1}{2} \int x^{2} \sin x \, dx \\
&\qquad \color{gray}\text{Now we'll do that same: "is this easier?" question}
\end{align}
$$

Not great, but maybe that's still useful... if we were to try to continue:

$$
\int x^{2}\sin x \, dx
$$


$$
\begin{align}
u=x^{2} && dv = \sin x \, dx \\
du = 2x\,dx && v = \textcolor{gray}{\int \sin x \, dx =} -\cos x
\end{align}
$$

$$
\begin{align}
\int x^{2}\sin x \, dx &= x^{2} (-\cos x) - \int- \cos x (2x) \, dx \\
&= -x^{2} \cos x + 2\textcolor{orange}{\int x\cos x \,dx}
\end{align}
$$

Oh! That part is where we started! Interesting 🤔

