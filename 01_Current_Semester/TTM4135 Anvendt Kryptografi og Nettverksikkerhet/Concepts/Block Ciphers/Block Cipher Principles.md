---
tags:
  - Concept
---
# Concept for [[Block Ciphers.md]]

* Symmetric key ciphers in which each block of plaintext is encrypted with the same key.
* A **block** is a set of plaintext symbols of fixed size. Typical block sizes for modern block ciphers are between 64 and 256 bits.
* In practice, block ciphers are used in certain configurations called **modes of operation**. 

## Notation

$$\begin{aligned}
P&: \text{Plaintext block (length $n$ bits)}\\
C&: \text{Ciphertext block (length $n$ bits)}\\
K&: \text{Key (length $k$ bits)}\\
C&= E(P,K):\text{Encryption Function}\\
P&= D(C,K):\text{Decryption Function}
\end{aligned}$$
## Design Criteria

1940s Claude Shannon discussed TWO important encryption techniques:
* **Confusion**, involves substitution to make relationship between the key and ciphertext as complex as possible.
* **Diffusion**, involves transformations that dissipate statistical properties of plaintext across the ciphertext.