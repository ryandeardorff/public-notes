---
{"dg-publish":true,"permalink":"/efficiency-operations/","dgHomeLink":true,"dgPassFrontmatter":false}
---

#graphics #cs 
> [[CS200 Hub - Computer Graphics I|CS200 Hub - Computer Graphics I]], [[Rasterization|Rasterization]], [[Elementary Raster Operations|Elementary Raster Operations]]

### `incrementX()`
Moves current location one pixel to the right.
$$
[\text{offset} \leftarrow \text{offset} + 3]
$$
```ad-info
title:Explaination
collapse:true
`offset(i,j) = Sj + 3i`
If we want to do adjacent pixels $\square \square$:
`offset(i+1,j) = Sj +3(i+1)= offset(i,j) + 3`
That's just adding 3!
```

### `decrementX()`
Moves one pixel to the left.
$$
[\text{offset} \leftarrow \text{offset} - 3]
$$

### `incrementY()`
Moves one pixel up
$$
[\text{offset} \leftarrow \text{offset} + S]
$$
(where $S$ is the [[Pixel Size and Scan Line Stride|stride]])

### `decrementY()`
Moves one pixel down
$$
[\text{offset} \leftarrow \text{offset} - S]
$$