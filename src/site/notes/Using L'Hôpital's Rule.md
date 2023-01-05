---
{"dg-publish":true,"permalink":"/using-l-hopital-s-rule/","dgHomeLink":true,"dgPassFrontmatter":false}
---

#math 
>[[MAT 150 Hub - Calc I|MAT 150 Hub - Calc I]], [[L'Hôpital's Rule|L'Hôpital's Rule]]

$$
\lim_{x\rightarrow 0} \frac{1-\cos{x}}{x^{2}} $$
Check it's an [[Indeterminates|indeterminate]]:
$$
\dots= \frac{1-\cos0}{0^{2}} = \frac{1-1}{0} = \frac{0^{+}}{0^{+}}
$$
It is 👍
$$
\lim_{x\rightarrow 0} \frac{(1-\cos(x))'}{(x^{2})'} = \lim_{x\rightarrow 0} \frac{\sin{x}}{2x} = \frac{\sin{0}}{2\cdot0} = \frac{0^{+}}{0^{+}}
$$
$$
\lim_{x\rightarrow0} \frac{(\sin{x})'}{(2x)'} = \lim_{x\rightarrow 0} \frac{\cos{x}}{2} = \frac{\cos{x}}{2}= \boxed{\frac{1}{2}}
$$