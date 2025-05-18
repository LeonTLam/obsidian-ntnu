---
tags:
  - Concept
---
# Concept for [[Classical Encryption Techniques.md]]

## Basic Cipher Operations
Most historical ciphers are based on a combin. of two basic operations:

**Transposition:** characters in plaintext are mixed up with each other (permuted).
**Substitution:** Each character (or set of char.) is replaced by a different character (or set of char.).

### Transposition ciphers
permutes characters usually in fixed period $d$ and permutation $f$.

Consider the plaintext as a matrix of rows of length $d$.

Generally transposition ciphers can permute rows or columns and output in row or column order.

#### Simple transposition cipher
Key pair is $d$ and $f$
Each block of $d$ char. is re-ordered using the permutation $f$.

There are $d!$ permutations of length $d$.
$$d!=d\times(d-1)\times(d-2)\times ...\times2\times1$$

#### Simple substitution ciphers
each char. in plaintext alphabet is replaced by char. in ciphertext alphabet defined by a substitution table. Also called **monoalphabetic substitution ciphers**.

NOTE
*transposition ciphers permute plaintext characters, while substitution ciphers permute alphabet characters.*

**permute**: rearrangement