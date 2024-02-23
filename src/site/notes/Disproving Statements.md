---
{"dg-publish":true,"permalink":"/disproving-statements/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

#math 
> [[MAT 258 Hub - Discrete Mathematics|MAT 258 Hub - Discrete Mathematics]]

If the statement is of the type "$\forall x P(x)$", we disprove it by finding a counterexample (one x in the domain so that $P(x)$ is F)
If the statement is of the type "$\exists x P(x)$", we disprove it by showing $P(x)$ is $F$ for all $x$ in the domain,
that is, we show $\forall x\, \neg P(X)$

### Ex 3
$p_{1}, p_{2}, p_{3}, \dots, p_{n}$ are the first few prime numbers.
$2,3,5,7,11,\dots$
Then $s=p_{1}\times p_{2}\times, \dots\times p_{n}+1$ is also prime.

$2+1 =3$ $\checkmark$
$2*3+1=5\checkmark$
$2*3*5+1=31\,\checkmark$
$2*3*5*7+1=211 \,\checkmark$
$2*3*5*7*11+1=2311\,\checkmark$
$2*3*5*7*11*13+1 = 30031$
$=59\times509$ <- not prime! We found a counterexample.

### Ex 4
For any two non-negative real numbers $a,b$ :
$\sqrt{a+b}=\sqrt{a}+\sqrt{b}$

Not true, counterexample : $a=1, b=9$
$\sqrt{1+9} = \sqrt{10}$ but
$\sqrt{1}+\sqrt{9} = 1+3 = 4$
and $\sqrt{10}\ne4$.

### Ex 5
There exists a positive integer $n$ so that $n^{2}+3n+2$ is prime

| $n$ | $n^{2}+3n+2$ |
| ---- | ---- |
| 1 | 6 |
| 2 | 12 |
| 3 | 20 |
| 4 | 30 |
| $\vdots$ |  |
They're all even, and larger than 2.

This is false. To  disprove, we show for all $n$ positive integers $n^{2}+3n+2$ is not a prime.

Since $n^{2}+3n+2 = (n+1)(n+2)$ which is even (b/c it is the product of two consecutive integers) and since $n \ge 1$ each of the factors is at least $2$, so $n^{2} +3n + 2 \gt 2$, which means $n^{2}+3n+2 \ne 2$. (so it is not the even prime).

### Ex 6
There exists an integer $n$ so that $n^{2}+3n+2$ is prime.
True, since for $n=0,\quad n^{2}+3n+2=2$ a prime.