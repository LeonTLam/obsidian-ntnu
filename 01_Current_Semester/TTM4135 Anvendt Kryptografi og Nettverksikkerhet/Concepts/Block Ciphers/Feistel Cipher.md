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
3. Ciphertext $C=W_r$ is defined by $C=(L_r,R_r)$.
![[{B41BF60D-7E0D-4097-B6F3-712CFA7354F2}.png]]
## Feistel Decryption
1. Write ciphertext block $C$ as $C = (L_r,R_r)$
2. For each round $r$ perform following:
$$\begin{aligned}
L_{i-1} &= R_i\oplus f(L_i,K_i)\\
R_{i-1} &= L_i
\end{aligned}$$