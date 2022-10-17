---
{"dg-publish":true,"permalink":"/mass-aggregate-physics-engines/","dgHomeLink":true,"dgPassFrontmatter":false}
---

#physics 
> [[Game Physics Research Hub|Game Physics Research Hub]]

Mass aggregate physics engines "treat objects as if they were made up of lots of little masses. A box might be simulated as if it were made up of eight masses, one at each corner, connected by rods". [source](https://learning.oreilly.com/library/view/game-physics-engine/9780123819765/chapter-15.html#:-:text=Mass%20aggregate%20engines%20tr,corner%2C%20connected%20by%20rods)

Because of this they are easier to program because they don't need to handle rotations-- it comes from the separation of masses.

### Problems:
Because of the separation of masses-- it is difficult to make really firm/solid objects in a mass aggregate system. Things will have a certain degree of flex. And to compensate for that becomes ugly.

