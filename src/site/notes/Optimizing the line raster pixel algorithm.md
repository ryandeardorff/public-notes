---
{"dg-publish":true,"permalink":"/optimizing-the-line-raster-pixel-algorithm/","dgHomeLink":true,"dgPassFrontmatter":false}
---

#graphics 
> [[CS200 Hub - Computer Graphics I|CS200 Hub - Computer Graphics I]], [[Line Rasterization|Line Rasterization]], [[Line Raster Pixel Algorithm|Line Raster Pixel Algorithm]], [[Elementary Raster Operations|Elementary Raster Operations]], [[Efficiency Operations|Efficiency Operations]]

$$
\begin{align}
\text{Observe}: \\
y(i) &= y_{0} + m(i-x_{0}) \\
y(i\textcolor{orange}{+1}) &= y_{0} + m((i+1) - x_{0}) \\
&= y_{0} + mi + m - mx_{0} \\
&= y_{0} + m(i-x_{0}) +m \\
&= y(i) + m
\end{align}
$$

This is noting that the previous pixel's calculation can be leveraged, computing the new point from the previous point and adding the slope.