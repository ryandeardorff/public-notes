---
{"dg-publish":true,"permalink":"/collision-detection/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

#physics #cs 
> [[Game Physics Research Hub|Game Physics Research Hub]]

A good way to structure the collisions in a physics engine is to have a "collision detector", which will use a collision detection algorithm to form a set of `Contact` data structures filled with appropriate information.

> "Collision detection obviously needs to take account of the *geometries* of the objects, that is, their shape and size. So far in the physics engine, we’ve assumed that we are dealing with *particles*, which lets us avoid taking any geometry into account
> 
> This is a distinction we’ll keep even with more complicated 3D objects: the **physics simulation** system (that part of the engine that handles [[Newton's Laws of Motion|laws of motion]], collision resolution, and [[Force|forces]]) will **not need to know the details of the shape of the objects** it is dealing with. The **collision detection** system is responsible for **calculating any properties that are geometric**, such as when and where two objects are touching, and the [[Contact Normal (Collision Direction)|contact normal]] between them."

[source](https://learning.oreilly.com/library/view/game-physics-engine/9780123819765/chapter-53.html#:-:text=In%20our%20engine%2C%20the%20end%20result%20of%20the%20collision%20detection%20algorithm%20is%20a%20set%20ofContactdata%20structures%20filled%20with%20the%20appropriate%20information.%20Collision%20detection%20obviously,122%20Chapter%207%20Hard%20Constraintsneeds%20to%20take%20account%20of%20the%20geometries%20of%20the%20objects%2C%20that%20is%2C%20their%20shape%20and%20size.%20Sofar%20in%20the%20physics%20engine%2C%20we%E2%80%99ve%20assumed%20that%20we%20are%20dealing%20with%20particles%2C%20which%20l%20etsus%20avoid%20taking%20any%20geometry%20into%20account.This%20is%20a%20distinction%20we%E2%80%99ll%20keep%20even%20with%20more%20complicated%203D%20objects%3A%20the%20physicssimulation%20system%20(that%20part%20of%20the%20engine%20that%20handles%20laws%20of%20motion%2C%20collision%20res-olution%2C%20and%20forces)%20will%20not%20need%20to%20know%20the%20details%20of%20the%20shape%20of%20the%20objects%20it%20isdealing%20with.%20The%20collision%20detection%20system%20is%20responsible%20for%20calculating%20any%20prop-erties%20that%20are%20geometric%2C%20such%20as%20when%20and%20where%20two%20objects%20are%20touching%2C%20and%20thecontact%20normal%20between%20them)
