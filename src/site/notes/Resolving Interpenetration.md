---
{"dg-publish":true,"permalink":"/resolving-interpenetration/","dgHomeLink":true,"dgPassFrontmatter":false}
---

#physics 
> [[Game Physics Research Hub|Game Physics Research Hub]]

Our goal is to move two objects apart just enough to separate them.

The [[Collision Detection|collision detector]] is responsible for figuring out [[Penetration Depth|how far they have interpenetrated]].

To resolve the interpenetration, we check the depth of it...
$$
\begin{align}
&\text{If it is already } \le 0 \rightarrow \text{No need to take action} \\
&\text{Otherwise, move the two objects apart, just far enough penetration depth}\\
&\text{becomes } 0.
\end{align}
$$

As noted in [[Penetration Depth|Penetration Depth]]:

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">

<div class="markdown-embed-title">



</div>


#physics 
> [[Game Physics Research Hub|Game Physics Research Hub]]

```ad-note
I will likely come back to this when researching more detection algorithms, for now this is just info on interpenetration depth as it relates to resolving collisions.
```

Just like [[Velocities of Separation and Approach (Closing Velocity)|Velocities of Separation and Approach (Closing Velocity)]], penetration depth has both **size** and **sign**.

Negative depth represents no interpenetration. Depth of 0 represents two objects merely touching.

The penetration depth provided by the [[Collision Detection|Collision Detection]] system should be depth of penetration **in the direction of the [[Contact Normal (Collision Direction)|Contact Normal (Collision Direction)]]**. ^45b0cb

</div></div>


So if we move the objects in the direction of the [[Contact Normal (Collision Direction)|Contact Normal (Collision Direction)]] by a distance equal to the penetration depth, they will no longer be in contact. Same with just one object involved in the contact (dynamic object colliding against static object). 

At that point, the only question is how much to move each object...

To mimic as close as we can the expected results (something like a box resting on a planet), we move the objects apart in an **inverse proportion to their mass**. Large mass object get almost no change, small mass object gets to move a lot:

$$
m_{a}\Delta p_{a} + m_{a}\Delta p_{b} = d
$$

We can rewrite these:
$$
\begin{align}
\Delta p_{a} = \frac{m_{b}}{m_{a}+m_{b}}d && && \Delta p_{b} = \frac{m_{a}}{m_{a}+m_{b}} d
\end{align}
$$

Which we then move along the [[Contact Normal (Collision Direction)|Contact Normal (Collision Direction)]]:
$$
\begin{align}
\Delta \vec{p}_{a} = \frac{m_{b}}{m_{a}+m_{b}}d \cdot \textcolor{orange}{\hat{n}} && && \Delta \vec{p}_{b} = \textcolor{orange}{-}\frac{m_{a}}{m_{a}+m_{b}}d \cdot \textcolor{orange}{\hat{n}}
\end{align}
$$
*Notice that $-$ btw in the second one, [[Contact Normal (Collision Direction)|Contact Normal (Collision Direction)]] is from object $a$'s perspective!*

[source](https://learning.oreilly.com/library/view/game-physics-engine/9780123819765/chapter-54.html#:-:text=Resolving%20Interpenetration)