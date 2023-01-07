---
{"dg-publish":true,"permalink":"/iterative-contact-resolution/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

#physics 
> [[Game Physics Research Hub|Game Physics Research Hub]]

Iterative contact resolution handles contacts one by one. This can make it fast to resolve.

### Problems
Because contacts are handled one by one, having one object affect another can sometimes have significant affects-- and not desirable ones. 

A more complicated and time consuming way to solve this is with [[Jacobian-Based Contact Resolution|Jacobian-Based Contact Resolution]]. But it's just that, more complicated and time consuming.

There is also [[Reduced-Coordinate Contact Resolution|Reduced-Coordinate Contact Resolution]], but this approach can be quite slow, so for games it's not often viable.

[source](https://learning.oreilly.com/library/view/game-physics-engine/9780123819765/chapter-15.html#:-:text=A%20more%20physically%20realist,ing%20with%20inconsistencies.)