---
tags:
  - Concept
---
# Concept for [[Block Ciphers.md]]

## Product Cipher
A product cipher is a cryptosystem in which encryption function is formed by applying several sub-encryption functions
Most block ciphers are the composition of simple functions $f_i$ for $i=1,...,r$ where each $f_i$ has a different key $K_i$.

$$C=E(P,K)=f_r(...(f_2(f_1(P,K_1),K_2)...),K_r)$$
## Iterated Cipher
Most modern blocks ciphers are in special class of product ciphers known as **iterated ciphers**.
* Encryption process divided into $r$ similar **rounds**.
* Sub-encryption functions are all same function, $g$, called **round function**.
* Each key $K_i$ derived from overall master key $K$. The keys $K_i$ are called **round keys** or **subkeys** and are derived from $K$ using a process called **key schedule**.

### Encryption in Iterated Cipher
Given plaintext block $P$, a round function $g$ and round keys $K_1, K_2,...,K_r$, the ciphertext block $C$, is derived through $r$ rounds:

$$\begin{aligned}
W_0 &= P\\
W_1 &= g(W_0,K_1)\\
W_2 &= g(W_1,K_2)\\
...\\
W_r&=g(W_{r-1},K_r)\\
C&=W_r
\end{aligned}$$
### Decryption in Iterated Cipher
Round function $g$ must have an inverse function $g^{-1}$ with $g_{-1}(g(W,K_i),K_i)=W$ for all keys $K_i$ and blocks $W$.
Decryption is simply the reverse of encryption.

$$\begin{aligned}
W_r&=C
W_{r-1} &= g^{-1}(W_r,K_r)\\
W_{r-2} &= g^{-1}(W_{r-1},K_{r-1})\\
...\\
W_0&=g^{-1}(W_{1},K_1)\\

\end{aligned}$$