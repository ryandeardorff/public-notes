---
{"dg-publish":true,"permalink":"/exploring-delta-time-with-vel-accel-and-pos/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

#physics 
> [[PHY200 Hub - Motion Dynamics|PHY200 Hub - Motion Dynamics]]

$$
\begin{align}
\Delta{t}\,\vec{a} &= \frac{\Delta\vec{v}}{\Delta t} \cdot \Delta t \\
\vec{a} \Delta t&= \Delta{\vec{v}}\\
\lim_{\Delta{t}\rightarrow0} \frac{\Delta \vec{v}}{\Delta t} &= \frac{d\vec{v}}{dt} \\
\vec{a} dt &= d\vec{v} \\
\int_{t=0}^{t=t} \vec{a} \, dt &= \int_{t=0}^{t=t} \vec{v} \,dt \\
\vec{a} \cdot t \bigg|_{t=0}^{t=t} &= \vec{v}(t) \bigg|_{t=0}^{t=t} \\
\vec{a}t &= \vec{v}(t)-\vec{v}(0) \\
\vec{v}(t) &= \vec{v}_{0} + \vec{a} t
\end{align}
$$
And remember, it's always a [[Vectors|vector]] with [[Expressing a vector with the cartesian unit vectors|individual components]].

We've basically made it to [[Euler Integration|Euler Integration]]!

And further $\Delta\vec{x}$

$$
\begin{align}
\Delta\vec{x} &= \vec{v}(t)\cdot\Delta t \\
\lim_{\Delta{t}\rightarrow0} \frac{\Delta{x}}{\Delta{t}} &= \frac{d\vec{x}}{dt} \\
\vec{v}(t) &= \frac{d\vec{x}}{dt} \\
\frac{d}{dt}(\vec{v}(t)) &= \frac{d}{dt}\left(\frac{d\vec{x}}{dt}\right) \\
\frac{d\vec{v}}{dt} &= \vec{a} = \frac{d^{2}\vec{x}}{dt^{2}}
\end{align}
$$

this is all very closely related to: [[Derivatives and Integrals for Physics|Derivatives and Integrals for Physics]]
