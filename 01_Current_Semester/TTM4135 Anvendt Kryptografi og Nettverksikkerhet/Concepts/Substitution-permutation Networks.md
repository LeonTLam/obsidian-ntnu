---
tags:
  - Concept
---
# Concept for [[Block Ciphers.md]]

A SPN is an iterated cipher.
The block length $n$ must allow each block to be split into $m$ sub-blocks of length $l$ so that $n=lm$. Two permutations are defined.
Permutation $\pi_s$ operates on sub-blocks of size $l$ bits.

$$\pi_s : \{0,1\}^l \rightarrow \{0,1\}^l$$ 
The permutation $\pi_s$ is normally called an S-box (substitution box).
Permutation $\pi_P$ swaps the inputs from {1, ..., n}. This is similar to transposition cipher.
$$\pi_P:\{1,2,...,n\} \rightarrow \{1,2,...,n\}$$
## Steps in SPN round function
Round function is defined by three steps
	1. Round key $K_i$ is XORd with the current state block $W_i$
	2. Each sub-block is replaced (substituted) by application of $\pi_S$ 
	3. The whole block is permuted using $\pi_P$