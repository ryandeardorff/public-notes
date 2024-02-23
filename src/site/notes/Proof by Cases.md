---
{"dg-publish":true,"permalink":"/proof-by-cases/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

#math 
> [[MAT 258 Hub - Discrete Mathematics|MAT 258 Hub - Discrete Mathematics]], [[Types of Proofs|Types of Proofs]]

Break problem into finitely many cases and prove each case by any method.

### Ex:
Sum of 2 consecutive integers is odd.
$0+1 =1$
$1+2 = 3$
$2+3 = 5$
$-1+(-2) = -3$

Proof:
Case 1:
- First integer is even $2k$
- Second integers is $2k+1$
- Sum = $2k+(2k+1) = 4k+1 = 2(2k)+1 = 2m+1$ is **odd**.
Case 2:
- First integer is odd $2k+1$
- Second integer is $2k+1+1 = 2k+2$
- Sum = $(2k+1)+(2k+2) = 4k+3 = 2(2k+1) + 1 = 2m+1$ is **odd**.
There are only these 2 cases, so we're done! You have to exhaust all cases.
*(this problem is much easier to solve with a [[Direct Proof|Direct Proof]], but can be done this way still!)*