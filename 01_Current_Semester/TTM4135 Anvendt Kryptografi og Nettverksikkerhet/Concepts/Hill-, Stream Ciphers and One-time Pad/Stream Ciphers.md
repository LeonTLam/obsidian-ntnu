---
tags:
  - Concept
---
# Concept for [[Hill cipher, Stream Ciphers and One-time Pad.md]]

Characterized by generation of a **keystream** of given length.
Each element of keystream used to encrypt one or more characters.

Usually symmetric key ciphers, where sender and receiver share same key and can generate same keystream given the same initialization value.
Keystream must have good randomness properties.

## Synchronous stream ciphers

Simplest kind of stream cipher, keystream generated independently of plaintext. 

Both sender and receiver need to generate same keystream and synchronize on its usage.

Vigenére cipher can be seen as a (periodic) synchronous stream cipher where each shift is defined by a key letter.

## Binary Synchronous stream cipher

For each time interval $t$, each of following are defined:
* Binary sequence $s(t)$ called keystream
* Binary plaintext $p(t)$
* Binary ciphertext $c(t)$
$$\begin{aligned}
\text{Encryption: }c(t)=p(t)\oplus s(t)
\end{aligned}$$