---
{"dg-publish":true,"permalink":"/rolling-a-dice-examples-of-probability/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

> [[MAT 258 Hub - Discrete Mathematics|MAT 258 Hub - Discrete Mathematics]]

### 1:
Roll `1D6`. Find prob. it lands on 6.

[[Experiment (Probability)|Experiment (Probability)]]: roll `1D6`
$\Omega$ = $\set{1,2,3,4,5,6}$
$E$ = land on $6$ = $\set{6}$

$$
P(E) = \frac{|E|}{|\Omega|} = \frac{1}{6}
$$
where $|E| =$ size of $E$
$|\Omega|$ = size of $\Omega$

### 2:
Roll `2D6`. Find probabilities:
a) P(two 6's) = 1/36
$$
\begin{align*}
\Omega &=  \left\{ \begin{array}{l} 11, 12,13,14,15,16
\\
21,22,23,24,25,26\\
\dots
\\
61,62,63,64,65,66\end{array}\right\}\\\\
\Omega&= 6^{2}=36
\end{align*}
$$

b) P(at least one 6) = 11/36
c) P(sum of 9) = 4/36
d) P(sum of 1) = 0/36
e)P(sum of 11) = 2/36


### 3:
Roll `2D6` let
$A=$ red lands on 6
$B=$ blue lands on 6
$E =$ at least one lands on 6.
Find probabilities:

$P(A)$, $P(B)$, $P(A\cap B)$, $PA\cup B$, $P(E)$, $P(E^{C})$

$P(A) = \frac{1}{6}$
$P(B) = \frac{1}{6}$
$P(A\cap B) = \frac{1}{36}$
$P(A\cup B) = \frac{11}{36}= P(A) + P(B) - P(A\cap B) = \frac{1}{6} +\frac{1}{6} + \frac{1}{36} = \frac{11}{36}$
$P(E^{C})=P(\text{none lands on }6)= \frac{5^{2}}{6^{2}} = \frac{25}{36}$
$P(E) = P(A\cup B) = \frac{11}{36} \text{ or } P(E)=1-P(E^{C}) = 1- \frac{25}{36}= \frac{11}{36}$

### 4:
Roll `100D6`
$A=$ no 6 in 100 rolls
$B=$ no 5 in 100 rolls
$E=$ at least one 6 in 100 rolls
$P(A),P(B),P(E),P(A\cap B),P(A\cup B)$

$P(A) = \frac{5^{100}}{6^{100}} = P(B)$
$P(E) = 1-P(E^{C})$ <-- we're looking at [[At least one or at most one side note (Probability)|At least one or at most one side note (Probability)]] $E^{C}=A$
$=1-P(A)$
$=1- \frac{5^{100}}{6^{100}}$

$P(A\cap B) = \frac{4^{100}}{6^{100}}$
$P(A\cup B) = P(A) + P(B) - P(A\cap B) = 2\times \frac{5^{100}}{6^{100}} - \frac{4^{100}}{6^{100}}$

### 5:

^ce34ec

Pick a card from deck of 52.
$A=$ card is spade
$B=$ card is a face (J,Q,K)

$P(A\cup B)$
So to compute, we compute:
$P(A)=\frac{1}{4}$
$P(B)= \frac{12}{52} = \frac{3}{13}$
$P(A\cap B) = \frac{3}{52}$
Going back up:
$P(A\cup B) = \frac{1}{4}+ \frac{3}{13} - \frac{3}{52} = \frac{22}{52}$

### 6:
Same setup as in [[Rolling a dice examples of probability#^ce34ec|5]]. Are $A$ and $B$ [[Independence (Probability)|independent]]?

$$
\begin{align*}
&P(A\cap B) = \frac{3}{52} \\
&P(A)\cdot P(B) = \frac{1}{4} \times \frac{3}{13} = \frac{3}{52}
\end{align*}
$$
$P(A\cap B) = P(A)\cdot P(B)$
Yes, independent.

### 7:
Roll `2D6`. Are $A$ and $B$ [[Independence (Probability)|independent]]?
a)
$A = 1^{st}$ die lands on 6
$B=2^{nd}$ die lands on 6
$P(A)=P(B)= \frac{1}{6}$
$P(A\cap B) = \frac{1}{36}$
$\frac{1}{36}=\frac{1}{6}\times \frac{1}{6} \rightarrow$ [[Independence (Probability)|independent]] 👍

b)
$A=1^{st}$ die lands on 6
$B=$ sum is 7 $\textcolor{gray}{=\set{16,25,34,43,52,61}}$

$P(A) = \frac{1}{6}$
$P(B) = \frac{6}{36}=\frac{1}{6}$
$P(A\cap B) = \frac{1}{36}$
$\frac{1}{36}= \frac{1}{6}\times \frac{1}{6} \rightarrow$ [[Independence (Probability)|independent]]

*this was just an edge case! that's why it was independent, even though it feels like it should be dependent.
Our intuition wasn't wrong per-say, but we need to check with math for cases like these!*

c)
$A=1^{st}$ die is 6
$B=$ sum of 9 $\textcolor{gray}{=\set{36,45,54,63}}$

$P(A)=\frac{1}{6}$
$P(B) = \frac{4}{36}=\frac{1}{9}$
$P(A\cap B) = \frac{1}{36}$
$\frac{1}{36}\ne \frac{1}{6}\times \frac{1}{9}\rightarrow$ **not** [[Independence (Probability)|independent]]
