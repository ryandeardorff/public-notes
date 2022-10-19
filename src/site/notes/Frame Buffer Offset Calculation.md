---
{"dg-publish":true,"permalink":"/frame-buffer-offset-calculation/","dgHomeLink":true,"dgPassFrontmatter":false}
---

#graphics #cs 
> [[CS200 Hub - Computer Graphics I|CS200 Hub - Computer Graphics I]], [[Frame Buffer Model|Frame Buffer Model]], [[Pixel Size and Scan Line Stride|Pixel Size and Scan Line Stride]]

Because of [[Pixel Size and Scan Line Stride|Pixel Size and Scan Line Stride]]
We calculate scan line offset as:
$$
\begin{align}
&\textbf{given:}\\
&\text{screen coordinates: }(i,j) \qquad
\text{scan line stride: }S\\
\\
&\boxed{\text{offset} = Sj + 3i} \\
&\qquad\qquad\qquad\,\uparrow \\
&\qquad\text{the } \textbf3 \text{ comes from the bytes per pixel}
\end{align}
$$
