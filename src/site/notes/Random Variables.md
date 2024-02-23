---
{"dg-publish":true,"permalink":"/random-variables/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

> [[MAT 258 Hub - Discrete Mathematics|MAT 258 Hub - Discrete Mathematics]]

Way to quantify the outcome of an [[Experiment (Probability)|experiment]].

Def: $X:\Omega\rightarrow\mathbb{R}$ is a function that takes input outcomes and outputs real values, and is described by its probability mass function (pmf) : $P(x=k)$ = probability that $x$ takes on the value $k$
With $\sum\limits_{\text{all }k} P(x=k)=1$

Def: The expected value of $x$ (expectation/mean/average) is given by:
$$
E[x] = \sum\limits_{\text{all }k} k P(x=k)
$$
is the weighted average of values for $x$.