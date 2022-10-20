---
{"dg-publish":true,"permalink":"/resting-contacts-microcollision-approach/","dgHomeLink":true,"dgPassFrontmatter":false}
---

#physics #cs 
> [[Game Physics Research Hub|Game Physics Research Hub]]

### The Problem
If we have something like a particle resting on the ground, the force of gravity will push it on frame 1, frame 2 the position will get updated, causing [[Resolving Interpenetration|penetrate]] the ground, generating a collision. The resolver will then apply the collision response giving the following velocity:
$$
\vec{v} = e \vec{v} = e 2 \vec{a} t
$$
That means that in frame 3 it will have an upward velocity, pushing it into the air.
Which may or may not be noticeable depending on the framerate.

### Solving It
We can do 2 things:
##### 1: Detecting the contact earlier
If we set our collision detector to return contacts nearly but not quite interpenetrating, we get a contact to work with after frame 1.
##### 2: Recognize when an object has velocities that only arise from forces acting for one frame.
Assuming we know the forces acting on an object (as we should since they get stored on the object by this point), then we can solve for what the velocity from just these forces would be:

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">

<div class="markdown-embed-title">



</div>


#physics 
> [[Game Physics Research Hub|Game Physics Research Hub]], [[Impulses|Impulses]]

Impulses are measured in $kgm/s$ (also known as Newtons --$Ns$). Knowing this we see that impulses are measured in units of force multiplied by time:
$
\frac{kgm}{s^{2}} \times s
$
So an impulse can be represented as force applied for some specific length of time, as in:
$
p = \vec{F}t
$

^e50426

This is useful for [[Resting Contacts (microcollision approach)|Resting Contacts (microcollision approach)]].

[source](https://learning.oreilly.com/library/view/game-physics-engine/9780123819765/chapter-53.html#:-:text=There%20is%20one%20more%20importa,t%20inthe%20following%20section)


</div></div>

Then:
$$
\begin{align}
&\text{If actual velocity of the object } \le^{\textcolor{red}*} p \leftarrow \text{(the value from the force conversion)}, \\
&\text{Then:}\\
\end{align}
$$
We know the particle was stationary last frame.
--Which is likely a resting contact.
So rather than performing the impulse value for a collision, we apply the impulse that would result in a $0$ [[Velocities of Separation and Approach (Closing Velocity)|separating velocity]].

$^{*}$*or slightly more, accounting for error.*

You could also look at this as a collision with a $0$ [[Coefficient of Restitution|Coefficient of Restitution]]. So, as closing velocity drops, [[Coefficient of Restitution|Coefficient of Restitution]] changes suddenly from being a bounce to a resting contact.


There's more detailed logic for how to handle this edge case [here](https://learning.oreilly.com/library/view/game-physics-engine/9780123819765/chapter-55.html#:-:text=128%20Chapter%207%20Hard%20ConstraintsVelocity%20and%20the%20Contact%20NormalWhen%20we%20have%20two%20objects%20in%20resting%20contact%2C%20we%20are%20interested%20in%20their%20relative%20velocityrather%20than%20the%20absolute%20velocity%20of%20either.%20The%20two%20objects%20might%20be%20in%20resting%20contactwith%20one%20another%20in%20one%20diretcion%2C%20but%20moving%20across%20each%20other%20in%20another%20direction.A%20box%20might%20be%20resting%20on%20the%20ground%2C%20even%20though%20it%20is%20skidding%20across%20the%20surface%20atthe%20same%20time.%20We%20want%20the%20vibrating%20contacts%20code%20to%20cope%20with%20pairs%20of%20objects%20thatare%20sliding%20across%20one%20another.%20This%20means%20we%20can%E2%80%99t%20use%20the%20absolute%20velocity%20of%20eitherobject.To%20cope%20with%20this%20situation%2C%20the%20velocity%20and%20acceleration%20calculations%20are%20all%20per-formed%20in%20the%20direction%20of%20the%20contact%20normal%20only.%20We%20first%20find%20the%20velocity%20in%20thisdirection%2C%20and%20test%20to%20see%20whether%20it%20could%20hav%20e%20been%20solely%20caused%20by%20the%20componentof%20the%20acceleration%20in%20the%20same%20direction.%20If%20so%2C%20then%20the%20velocit%20y%20is%20changed%20so%20there%20isno%20separating%20or%20closing%20velocity%20in%20this%20direction.%20There%20still%20may%20be%20relative%20velocityin%20any%20other%20direction%3A%20but%20it%20is%20ignored.We%20can%20add%20this%20special%20case%20code%20to%20the%20collision%20processing%20function%20in%20the%20fol-lowing%20way%3AExcerpt%20from%20file%20src%2Fpcontacts.cppvoid%20ParticleContact%3A%3AresolveVelocity(real%20duration)%7B%2F%2F%20Find%20the%20velocity%20in%20the%20direction%20of%20the%20contact.real%20separatingVelocity%20%3D%20calculateSeparatingVelocity()%3B%2F%2F%20Check%20if%20it%20needs%20to%20be%20resolved.if%20(separatingVelocity%20%3E%200)%7B%2F%2F%20The%20contact%20is%20either%20separating%2C%20or%20stationary%3B%20there%E2%80%99s%2F%2F%20no%20impulse%20required.return%3B%7D%2F%2F%20Calculate%20the%20new%20separating%20velocity.real%20newSepVelocity%20%3D%20-separatingVelocity%20*%20restitution%3B%2F%2F%20Check%20the%20velocity%20buildup%20due%20to%20acceleration%20only.Vector3%20accCausedVelocity%20%3D%20particle%5B0%5D-%3EgetAcceleration()%3Bif%20(particle%5B1%5D)%20accCausedVelocity%20-%3D%20particle%5B1%5D-%3EgetAcceleration()%3Breal%20accCausedSepVelocity%20%3D%20accCausedVelocity%20*%20contactNormal*%20duration%3B%2F%2F%20If%20we%E2%80%99ve%20got%20a%20closing%20velocity%20due%20to%20aceleration%20buildup%2C%2F%2F%20remove%20it%20from%20the%20new%20separating%20velocity.if%20(accCausedSepVelocity%20%3C%200),7.2%20Collision%20Processing%20129%7BnewSepVelocity%20%2B%3D%20restitution%20*%20accCausedSepVelocity%3B%2F%2F%20Make%20sure%20we%20haven%E2%80%99t%20removed%20more%20than%20was%2F%2F%20there%20to%20remove.if%20(newSepVelocity%20%3C%200)%20newSepVelocity%20%3D%200%3B%7Dreal%20deltaVelocity%20%3D%20newSepVelocity%20-%20separatingVelocity%3B%2F%2F%20We%20apply%20the%20change%20in%20velocity%20to%20each%20object%20in%20proportion%20to%2F%2F%20their%20inverse%20mass%20(i.e.%2C%20those%20with%20lower%20inverse%20mass%20%5Bhigher%2F%2F%20actual%20mass%5D%20get%20less%20change%20in%20velocity).real%20totalInverseMass%20%3D%20particle%5B0%5D-%3EgetInverseMass()%3Bif%20(particle%5B1%5D)%20totalInverseMass%20%2B%3D%20particle%5B1%5D-%3EgetInverseMass()%3B%2F%2F%20If%20all%20particles%20have%20infinite%20mass%2C%20then%20impulses%20have%20no%20effect.if%20(totalInverseMass%20%3C%3D%200)%20return%3B%2F%2F%20Calculate%20the%20impulse%20to%20apply.real%20impulse%20%3D%20deltaVelocity%20%2F%20totalInverseMass%3B%2F%2F%20Find%20the%20amount%20of%20impulse%20per%20unit%20of%20inverse%20mass.Vector3%20impulsePerIMass%20%3D%20contactNormal%20*%20impulse%3B%2F%2F%20Apply%20impulses%3A%20they%20are%20applied%20in%20the%20direction%20of%20the%20contact%2C%2F%2F%20and%20are%20proportional%20to%20the%20inverse%20mass.particle%5B0%5D-%3EsetVelocity(particle%5B0%5D-%3EgetVelocity()%20%2BimpulsePerIMass%20*%20particle%5B0%5D-%3EgetInverseMass())%3Bif%20(particle%5B1%5D)%7B%2F%2F%20Particle%201%20goes%20in%20the%20opposite%20direction.particle%5B1%5D-%3EsetVelocity(particle%5B1%5D-%3EgetVelocity()%20%2BimpulsePerIMass%20*%20-particle%5B1%5D-%3EgetInverseMass())%3B%7D%7DTo%20keep%20two%20objects%20in%20resting%20contact%2C%20we%20are%20applying%20a%20small%20change%20in%20velocityateachframe.Thechangeisjustbigenoughtocorrecttheincreaseinvelocitythatwould%20arise%20from%20them%20settling%20into%20one%20another%20over%20the%20course%20of%20one%20frame)


[source](https://learning.oreilly.com/library/view/game-physics-engine/9780123819765/chapter-54.html#:-:text=Resting%20Contacts)