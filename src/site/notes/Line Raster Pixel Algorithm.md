---
{"dg-publish":true,"permalink":"/line-raster-pixel-algorithm/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

#graphics 
> [[CS200 Hub - Computer Graphics I|CS200 Hub - Computer Graphics I]], [[Line Rasterization|Line Rasterization]], [[Elementary Raster Operations|Elementary Raster Operations]], [[Rasterization|Rasterization]]

Note this: [[Optimizing the line raster pixel algorithm|Optimizing the line raster pixel algorithm]]!
$$
\begin{align}
&\text{Algorithm for } |m| \le 1 \text{ and } \Delta{x}\gt 0\\
&\quad\textcolor{gray}{(\text{other 3 cases are similar})}\\
\hline
\end{align}
$$

$$
\begin{align}
&i_{min} = \text{round}(x_{0}) \\
&i_{max} = \text{round}(x_{1}) \\
\\
&\text{for } i = i_{min} \text{ to } i_{max}: \\
&\quad\quad  y = y_{0}+ m(i-x_{0}) \\
&\quad\quad  j = \text{round}(y) \\
&\quad\quad  \text{gotoPoint}(i,j) \\
&\quad\quad  \text{writePixel}() \\
\end{align}
$$

```cpp
for i :[i_min to i_max):
	y = y_0 + m*(i-x_0)
	j = round(y)
	gotoPoint(i,j)
	writePixel()
```
