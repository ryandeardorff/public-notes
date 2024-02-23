---
{"dg-publish":true,"permalink":"/binary-combinations/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

> [[MAT 258 Hub - Discrete Mathematics|MAT 258 Hub - Discrete Mathematics]]

String of binary (1 or 0), length of 6, how many combinations:
(0) full string
$2^{6}$
(a) start with 1
$2^{5}$
(b) end with 00
$2^{4}$
(c) start with 1 and end with 00
$2^{3}$

(d) string starts with 1 **or** ends in 00

$2^{5}+2^{4}-2^{3}$ <-- $2^{3}$ was the **overlap**

strings from (c) were included in both (a) and (b).