---
{"dg-publish":true,"permalink":"/rewriting-compound-propositions-with-negation/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

> [[MAT 258 Hub - Discrete Mathematics|MAT 258 Hub - Discrete Mathematics]], [[De Morgan Laws (negation)|De Morgan Laws (negation)]], [[Proposition|Proposition]], [[Predicates|Predicates]]

Write the following [[Compound Propositions and Connectives|compound propositions]] so that [[De Morgan Laws (negation)|neg]] is only in front of the [[Predicates|predicate]]

1) $\neg\, \exists\, x (P(x)\wedge Q(x) \lor \neg R(x))$
$\forall x \neg((P(x)\wedge Q(x))\lor \neg R(x))$
$\forall x (\neg(P(x)\land Q(x))\wedge \neg (\neg R(x)))$
$\forall x((\neg P(x)\lor\neg Q(x))\land R(x))$

2) $\neg \forall x (P(x) \rightarrow Q(x))$

$\exists x \neg (P(x)\rightarrow Q(x))$ 
$\exists x \neg(\neg P(x) \lor Q(x))$ < -- [[Implication (Conditional)|Implication (Conditional)]], [[Negation of Implication|Negation of Implication]]
$\exists x (\neg\neg P(x)\land \neg Q(x))$
$\exists x (P(x \land \neg Q(x)))$