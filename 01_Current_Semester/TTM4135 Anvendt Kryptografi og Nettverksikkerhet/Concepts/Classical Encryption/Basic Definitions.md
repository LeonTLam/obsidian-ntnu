---
tags:
  - Concept
---
# Concept for [[Classical Encryption Techniques.md]]

# Cryptography
*The study of designing cryptosystems.*

# Cryptanalysis
*The study of breaking cryptosystems*

# Confidentiality and Authentication
Cryptography, transformation of data depending on secret called **key**.

Used to provide confidentiality and authentication (or integrity).

**Confidentiality** - key needed to **read** message.
**Authentication** - key needed to **write** message.

# Cryptosystems

Consists of:
* set of plaintexts (original message)
* set og ciphertexts (encrypted message)
* set of keys
* function transforming plaintext to ciphertext (encryption)
* inverse function transforming ciphertext to plaintext (decryption)

# Symmetric and Asymmetric Cryptography

## Symmetric key cipher (secret key cipher)
Encryption and decryption keys known only to sender and receiver
**Requires** secure channel for transmission of cryptographic key.
### Notation

$$\begin{aligned}
E &= \text{Encryption function}\\
D &= \text{Decryption function}\\
M &= \text{Message/Plaintext}\\
C &= \text{Cryptogram/Ciphertext}\\
K &= \text{Shared secret key}\\
\\
\text{Encryption}: C&=E(K,M)\\
\text{Decryption}: M&=D(K,C)
\end{aligned}$$

## Asymmetric key cipher (public key cipher)
Each participant has a public and private key.
Allows both encryption and creation of digital signatures.


