---
{"dg-publish":true,"permalink":"/negation-of-implication/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

>[[MAT 258 Hub - Discrete Mathematics|MAT 258 Hub - Discrete Mathematics]]

The negation of $p\rightarrow q$ is $p\wedge\neg\,q$

### Explaination
We cannot translate it directly into an if-then, it's something else.
But we can use the 
<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">

<div class="markdown-embed-title">



</div>


> [[MAT 258 Hub - Discrete Mathematics|MAT 258 Hub - Discrete Mathematics]]

Given propositions $p$ and $q$, $p\rightarrow q$ is called an **implication** or conditional.

- $p$ is the premise or antecedent
- $q$ is the conclusion or consequence

- If $p$ is False, then $p\rightarrow q$ is True <------ this is the surprising one.
- if $p$ is T and $q$ is T, then $p\rightarrow q$ is T
- if $p$ is T and $q$ is F, then $p\rightarrow q$ is F.


$p\rightarrow q$ is logically equivalent to $\neg\,p \lor q$ ^6f291b

Simplified
$F\rightarrow F$ is T
$F \rightarrow T$ is T
$T\rightarrow T$ is T
$T\rightarrow F$ is F ^e168c9

</div></div>

To then negate that instead:

| p | q | $p\rightarrow q$ | $\neg\,(p\rightarrow q)$ |
| ---- | ---- | ---- | ---- |
| T | T | T | F |
| T | F | F | F |
| F | T | T | F |
| F | F | T | F |
$\neg\, (p\rightarrow q)$ is equivalent to $\neg\,(\neg p \lor q)$. How do we simplify? Use [[De Morgan Laws (negation)|De Morgan Laws (negation)]]

$$
\neg(p\rightarrow q) \equiv \neg\,(\neg\,p\lor q) \equiv \neg\neg\,p \wedge \neg\,q \equiv p\wedge \neg\,q
$$