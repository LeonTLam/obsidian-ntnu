---
tags:
  - Concept
---
# Concept for [[Block Ciphers.md]]

A SPN is an iterated cipher.
The block length $n$ must allow each block to be split into $m$ sub-blocks of length $l$ so that $n=lm$. Two permutations are defined.
Permutation $\pi_s$ operates on sub-blocks of size $l$ bits.

$$\pi_s : \{0,1\}^l \rightarrow \{0,1\}^l$$ 
The permutation $\pi_s$