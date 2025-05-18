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
\text{where }n=26 \text{ or } n=27 \text{ (size of alphabet)}
\end{aligned}$$
### Cryptanalysis of Caesar Cipher

Only need to find where one of the most frequent characters is shifted to.

Suppose ciphertext:

$$\text{PACGHJUHHCRICGRFWRUCRICPHGLFLQH}$$
First, count characters. Most common characters are C and H with freq. 5 each.

If we assume space "∇" is in the alphabet, we try:

1. ∇ -> H, j=8 since ∇= 0.
$$\text{HTVZ∇BM∇∇VJA. . .}$$
	Not correct, no recognizable words and double white-space.

2. ∇ -> C, j=3