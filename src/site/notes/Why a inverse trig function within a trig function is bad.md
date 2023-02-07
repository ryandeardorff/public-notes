---
{"dg-publish":true,"permalink":"/why-a-inverse-trig-function-within-a-trig-function-is-bad/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

#math 
> [[MAT 200 Hub - Calc II|MAT 200 Hub - Calc II]]

$$
\cos(\arcsin x)
$$
is bad.

---
If we were letting $x=\sin\theta$ and writing $\cos\theta$ in terms of x:
Solve for $\theta$: 
$\theta = \arcsin x$
We'd get
$$
\cos\theta = \cos(\arcsin x)
$$
but why not use the trig identity [[Important Trig Identities|Important Trig Identities]]:
$$
\cos\theta = \sqrt{1-\sin^{2}\theta} = \sqrt{1-x^{2}}
$$
much better!