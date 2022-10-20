---
{"dg-publish":true,"permalink":"/penetration-depth/","dgHomeLink":true,"dgPassFrontmatter":false}
---

#physics 
> [[Game Physics Research Hub|Game Physics Research Hub]]

```ad-note
I will likely come back to this when researching more detection algorithms, for now this is just info on interpenetration depth as it relates to resolving collisions.
```

Just like [[Velocities of Separation and Approach (Closing Velocity)|Velocities of Separation and Approach (Closing Velocity)]], penetration depth has both **size** and **sign**.

Negative depth represents no interpenetration. Depth of 0 represents two objects merely touching.

The penetration depth provided by the [[Collision Detection|Collision Detection]] system should be depth of penetration **in the direction of the [[Contact Normal (Collision Direction)|Contact Normal (Collision Direction)]]**. ^45b0cb