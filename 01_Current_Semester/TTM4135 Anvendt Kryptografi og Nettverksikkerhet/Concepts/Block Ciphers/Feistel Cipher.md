---
tags:
  - Concept
---
# Concept for [[Block Ciphers.md]]

An iterated cipher in which the round function swaps the two halves of the block and forms a new right hand half.

## Feistel Encryption
1. Split plaintext block $P=W_0$ into two halves: $W_0=(L_0, R_0)$.
2. For each round $r$ perform following:
$$\begin{aligned}
L_i &= R_{i-1}\\
R_i &= L_{i-1}\oplus f(R_{i-1},K_i)
\end{aligned}$$
