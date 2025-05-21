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

## Vernam OTP (Binary)

Binary Sequence:
* Plaintext: $b_1,...b_r$
* Keystream random: $k_1,...,k_r$
* Ciphertext: $c_1,...,c_r$
$$\begin{aligned}
\text{Encryption: }c_i\equiv p_i \oplus k_i\\
\text{Decryption: }p_i\equiv c_i \oplus k_i\\
\end{aligned}$$
Length of keystream = length of plaintext
Perfect secrecy, because any ciphertext has equal probability given plaintext.
Encryption and decryption are identical processes.

## Properties

* Perfect secrecy requires as many keys as messages
* OTP is considered the only unbreakable cipher
* Main problem is management of  completely random keys
* Generation, transportation, synchronization and destruction is problematic due to key size being large
* Only practical between known sender and receiver AFTER key has been securely distributed beforehand (pre-assigned communication).

## Key management issues for OTP

**How to generate completely random keys?**
* True random number generators (TRNGs), radioactive decay, atmospheric noise, etc.
* Pseudorandom number generators (PRNGs), not sufficient as they are deterministic.

**How to transport random keys between sender and receiver?**
* In-person handover
* Physical media

* Over secure channels, but defeats the purpose of OTP's simplicity.

**How to synchronize on usage of keys**
* Keep a shared key index or counter to track usage of a key
* Strictly ensure no key reuse
* Timestamps, message IDs, or sequence numbers

**How to destroy keys after use?**
* Overwrite memory/storage multiple times
* Physically destroy media