---
{"dg-publish":true,"permalink":"/velocity-verlet-integration/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

#physics 
> [[Game Physics Research Hub|Game Physics Research Hub]], [[Physics Integration|Physics Integration]], [[Euler Integration|Euler Integration]]

[[Euler Integration|Euler Integration]] can become inaccurate over long periods of time, so we can use **Velocity Verlet Integration** to compensate for this. We just need to take the *previous velocity* into account.

$$
P = \frac{V_{\text{old}} + V}{2} \Delta t
$$

^22d708

[source](https://learning.oreilly.com/library/view/game-physics-cookbook/9781787123663/ch14s07.html#:-:text=Taking%20the%20old%20velocity%20i,locity%20Verlet%20Integration)