---
{"dg-publish":true,"permalink":"/specifying-camera-orientation/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

#graphics 
> [[CS250 Hub - Graphics II|CS250 Hub - Graphics II]], [[3D Camera Model|3D Camera Model]]

$\vec{l}$ = look-at vector *(not necessarily unit)*
$\vec{r}$ = relative (global) up vector. *this is independent of any camera-- it's a global up*

We're looking to get $(\vec{u},\vec{v},\vec{n})$ as defined in [[3D Camera Data|3D Camera Data]].

We can get the camera orientation from:
$$
\boxed{
\vec{n} = \frac{-\vec{l}}{\|{\vec{l}}\|} \qquad\quad
\vec{u} = \frac{\vec{l}\times\vec{r}}{\|\vec{l}\times\vec{r}\|} \qquad\quad
\vec{v} = \vec{n}\times\vec{u}
}
$$

### Rationale:
The $\vec{l}$ is opposite the back vector $\vec{n}$
So if we think about it:
$$
\vec{n} = \frac{-\vec{l}}{\|{\vec{l}}\|}
$$

Then to get the right vector $\vec{u}$
We want to get [[The Cross Product|The Cross Product]] of $\vec{l}$ and $\vec{r}$ since that will give us the vector orthogonal to both. [[Cross Product orthogonality|Cross Product orthogonality]]:

$$
\vec{u} = \frac{\vec{l}\times\vec{r}}{\|\vec{l}\times\vec{r}\|}
$$

Then now that we know two of the 3, we can just do [[The Cross Product|The Cross Product]] due to [[Cross Product orthogonality|Cross Product orthogonality]]. And we don't even need to normalize it since the other two vectors are already [[Unit Vectors|Unit Vectors]].

$$
\vec{v} = \vec{n}\times\vec{u}
$$