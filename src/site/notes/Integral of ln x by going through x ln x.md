---
{"dg-publish":true,"permalink":"/integral-of-ln-x-by-going-through-x-ln-x/","dgHomeLink":true,"dgPassFrontmatter":false}
---

#math 
>[[MAT 150 Hub - Calc I|MAT 150 Hub - Calc I]], [[The Integral|The Integral]]

$$
\int \ln x \ dx 
$$

This is ***Almost*** :
$$
\int \ln x \ dx = x\ln x \quad ??
$$
$$
\frac{d}{dx} x \ln x = \frac{dx}{dx}\ln x + x \frac{d\ln{x}}{dx} = \ln{x} + 1
$$
We want to get rid of that $1$!

$$
\frac{d}{dx}(x\ln x - x) = (\ln x + 1) - \frac{dx}{dx} = \ln x + 1 - 1 = \boxed{\ln x}
$$

Look at that!

$$
\int \ln x \ dx =  \ln x - x + C
$$