---
{"dg-publish":true,"permalink":"/methods-of-partial-fraction-decomposition/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

#math 
> [[MAT 200 Hub - Calc II|MAT 200 Hub - Calc II]], [[Partial Fractions|Partial Fractions]]

## Method 1
$$
\begin{align}
\frac{3x-2}{(x-1)(x-4)}&= \frac{A}{x-1}+ \frac{B}{x-4}\\
\frac{3x-2}{(x-1)(x-4)}\textcolor{orange}{(x-1)(x-4)} &= \dots(x-1)(x-4)\\
3x-2&= A(x-4)+B(x-1)\\
\textcolor{orange}3x\textcolor{red}{-2} &= \textcolor{orange}{(A+B)}x+ \textcolor{red}{(-4A-B)}
\end{align}
$$

$$
\begin{cases}
A+B = 3 \\
-4A-B = -2
\end{cases}
$$
That's solving 2 systems of equations.

## Method 2

^ea91a3

$$
\begin{align}
3x-2&= A(x-4)+B(x-1)\\
\end{align}
$$
Plug in 2 different values of x.
Try: $x=0$:
$$
\begin{align}
-2=A(0-4)+B(0-1) \\
-2=-4A-B
\end{align}
$$
$x=1$:
$$
\begin{align}
3\cdot1 - 2 = A(1-4)+B(1-1) \\
1=-3A \rightarrow \boxed{A=\frac{-1}{3}}
\end{align}
$$
*Huh, would you look at that*
$x=4$:
$$
\begin{align}
3\cdot 4 - 2 = A(4-4) + B(4-1) \\
10=3B\rightarrow\boxed{B=\frac{10}{3}}
\end{align}
$$
*Wild!*

We just needed to use the **asymptotes**!
Look back at:
$$
\frac{\dots}{(x-1)(x-4)}
$$
Yep!

## Method 3
Basically [[Methods of Partial Fraction Decomposition#^ea91a3|Method 2]], but taking shortcuts
$$
\begin{align}
\frac{3x-2}{(x-1)(x-4)}&= \frac{A}{x-1}+ \frac{B}{x-4}\\
\end{align}
$$

What happens if we just plug in our roots right away ($1$ and $4$):
$x=1:$
$$
\begin{align}
\frac{3\cdot1-2}{(1-1)(1-4)} &= \frac{A}{1-1}+ \frac{B}{1-4} \\
\frac{3\cdot1-2}{1-4} &= A
\end{align}
$$
We can remove anything that doesn't have the 0 in the denominator
It's weird.
$$
A= \frac{1}{-3}, A= - \frac{1}{3}
$$
Same idea for $B$