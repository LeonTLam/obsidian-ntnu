---
tags:
  - Concept
---
# Concept for [[Classical Encryption Techniques.md]]

## Caesar Cipher

Moves the $i$-th letter of an alphabet to the $(i+j)$-th letter. The key is the value $j$..

Instead of writing out the whole substitution table, we can define encryption and decryption as follows:

$$\begin{aligned}
\text{Encryption: }c_i = (a_i+j)\bmod n\\
\text{Decryption: }a_i = (c_i-j)\bmod n\\
\text{where }
\end{aligned}$$
