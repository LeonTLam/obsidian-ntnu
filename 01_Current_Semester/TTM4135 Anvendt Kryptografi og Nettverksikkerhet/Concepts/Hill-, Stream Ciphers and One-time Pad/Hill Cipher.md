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
$$\begin{aligned}$$
