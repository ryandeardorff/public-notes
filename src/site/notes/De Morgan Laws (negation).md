---
{"dg-publish":true,"permalink":"/de-morgan-laws-negation/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

> [[MAT 258 Hub - Discrete Mathematics|MAT 258 Hub - Discrete Mathematics]], [[Truth Tables|Truth Tables]], [[Logical Equivalence|Logical Equivalence]], [[Compound Propositions and Connectives|Compound Propositions and Connectives]]

1.  $\neg\,(p\wedge q) \equiv \neg\,p \lor \neg\,q$
2. $\neg\,(p\lor q) \equiv \neg\,p\wedge\neg\,q$
Then for [[DeMorgan Laws for Quantifiers|negation of quantifiers]]
3. $\neg\, \forall x\,P(x) \equiv \exists x \,\neg \,P(x)$
4. $\neg\,\exists x \,P(x)\equiv \forall x \,\neg \,P(x)$


Proof of 1:

| $p$ | $q$ | $p\wedge q$ | $\neg\,(p\wedge q)$ | $\neg\,p$ | $\neg\,q$ | $\neg\,p\lor\neg\,q$ | $(\neg\,(p\wedge q))\leftrightarrow(\neg\,p\lor\neg\,q)$ |
| ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| T | T | T | F | F | F | F | T |
| T | F | F | T | F | T | T | T |
| F | T | F | T | T | F | T | T |
| F | F | F | T | T | T | T | T |
