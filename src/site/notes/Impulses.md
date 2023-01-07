---
{"dg-publish":true,"permalink":"/impulses/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

#physics 
> [[Game Physics Research Hub|Game Physics Research Hub]], [[A good example for Forces vs Impulses|A good example for Forces vs Impulses]]

In order to resolve a collision we only need to change velocity. 

Acceleration changes velocity by an amount depending on time. Here our changes are **instant**.
The **duration of the frame shouldn't affect the result**.

$$
p = m \cdot v
$$

Where $p$ is the **impulse**, $m$ is the mass, and $v$ is the [[Velocity|Velocity]].

The impulse can only *change* the velocity, it is not completely responsible for it. Such as the case where we use [[D'Alembert's Principle|D'Alembert's Principle]] with impulses (which we can do!):
$$
v' = v + \frac{1}{m}\sum\limits_{n} p_{i} = v + \frac{1}{m}(p_{i}+\dots + p_{n})
$$
We can sum up the impulses, but we have to remember the [[Velocity|Velocity]] is still there, the sum of the impulses with [[D'Alembert's Principle|D'Alembert's Principle]] is $\ne$ to the new velocity, it just affects it.