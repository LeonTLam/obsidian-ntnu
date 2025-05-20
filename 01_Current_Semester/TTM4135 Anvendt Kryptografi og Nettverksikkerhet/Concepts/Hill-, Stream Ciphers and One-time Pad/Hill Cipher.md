---
tags:
  - Concept
---
# Concept for [[Hill cipher, Stream Ciphers and One-time Pad.md]]

Hill Cipher is an example of **polygram cipher (polygraphic cipher).** A simple substitution cipher on an extended alphabet, multiple characters. Simplest example, is digram substitution, consisting of all pairs of characters.
Major weakness is linearity, known plaintext attacks easy.

## Definition

Hill Cipher performs a linear transformation on $d$ plaintext characters to get $d$ ciphertext characters.

* Encryption involves multiplying a $d\times d$ matrix $K$ by the block of plaintext $P$
* Decryption involves multiplying the matrix $K^{-1}$ by the block of ciphertext $C$
$$\begin{aligned}
\text{Encryption: } C=KP\\
\text{Decryption: } P=K^{-1}C
\end{aligned}$$
## Example Encryption

1. Choose $d=2$, encryption takes **digrams** as input and output blocks
2. Write each plaintext pair as a column vector and encode letters as numbers.
3. Suppose first pair is (EG). $E=4 \text{ and } G=6$, presented as $\begin{pmatrix} 4 \\ 6  \end{pmatrix}$
4. If not enough letters to fill block, use padding with uncommon letters such as Z-
5. This example includes "space" characters, all computation includes modulo 26.
