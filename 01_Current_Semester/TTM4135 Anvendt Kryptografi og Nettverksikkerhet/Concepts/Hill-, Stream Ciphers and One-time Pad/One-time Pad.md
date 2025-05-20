---
tags:
  - Concept
---
# Concept for [[Hill cipher, Stream Ciphers and One-time Pad.md]]

Truly random sequence of characters, all of them independently generated.

Key used only once.

Alphabet can be of any length, usually either natural language alphabet or binary alphabet (0,1).

Binary alphabet one-time pad is a (non-periodic) binary synchronous stream cipher.

Provides **perfect secrecy** when requirements are met:
* Key is truly random
* Used only once
* Kept secret

## OTP using Roman Alphabet

Plaintext char: $p_1,...,p_r$
Ciphertext char: $c_1,...,c_r$
Keystream, true random char: $k_1,...,k_r$

$$\begin{aligned}
\text{Encryption: }c_i=(p_i+k_i)\bmod26\\
\text{Decryption: }p_i=(c_i-k_i)\bmod26\\
\end{aligned}$$
### Example

Plaintext:    HELLO
Keystream: EZABD
Ciphertext: LDLMR

Any message could be sent with ciphertext **LDLMR**, depending on the choice of keystream.