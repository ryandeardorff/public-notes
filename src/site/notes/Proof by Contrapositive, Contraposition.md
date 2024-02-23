---
{"dg-publish":true,"permalink":"/proof-by-contrapositive-contraposition/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

#math 
> [[MAT 258 Hub - Discrete Mathematics|MAT 258 Hub - Discrete Mathematics]], [[Types of Proofs|Types of Proofs]], [[More Propositions - Contrapositive, Converse, Biconditional|More Propositions - Contrapositive, Converse, Biconditional]]

We want to show $p\rightarrow q$ but we prove instead $\neg\,q\rightarrow\neg\,p$.
(can do this because $(p\rightarrow q) \equiv (\neg\, q \rightarrow \neg\, p)$)
[[More Propositions - Contrapositive, Converse, Biconditional|More Propositions - Contrapositive, Converse, Biconditional]]

Ex: If $n^{2}+1$ is odd, then $n$ is even. ($n$ is an integer, implied by "even" in the statement.)
Proof:
(try [[Direct Proof|Direct Proof]])
- Since $n^{2}+1$ is odd, there is some $k\in\mathbb{Z}$ ($k$ is an integer)
- So that $n^{2}+1 = 2k+1$
- Then $n^{2} = 2k$
- So $n=\sqrt{2k}$ <----- *well that may not even be an integer! Let alone even!*
- We're stuck!
(proof by contrapositive)
- If $n$ is not even, then $n^{2}+1$ is not odd.
- If $n$ is odd, then $n^{2}+1$ is even.
- Since $n$ is odd, there is some integer $k$ so that $n=2k+1$.
- Then $n^{2}+1 = (2k+1)^{2}+1 = 4k^{2}+4k+1+1$
- So $n^{2}+1 = 2(2k^{2}+2k+1) = 2k\,'$
  where $k\,' = 2k^{2}+2k + 1$ is an integer
- Which means, $n^{2}+1$ is even.
- We did it! Proof by Contrapositive!