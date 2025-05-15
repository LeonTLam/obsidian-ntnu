---
tags:
  - Concept
---
# Concept for [[Classical Encryption Techniques.md]]


## Methods

There are many methods available to an adversary who wishes to break a cryptosystem. In general we consider the following:

* What resources the adversary has available. Computational capability and access to various inputs and outputs of the system.
* What they are aiming to achieve. Retrieving the whole of the secret key or little as distinguishing two messages (yes or no).

### Exhaustive key search

Most basic method of attack, also known as **brute-force attack**. Tries all possible keys.

Cannot prevent such attack, so all cryptosystems must have enough keys to make exhaustive search more difficult computationally.

**Note that:**
* Key can be found without exhaustive search
* May break cryptosystem without finding key
* Prevention is **minimum standard**

## Attack classification

1. **Ciphertext Only attack**: intercepted ciphertext is only available
2. **Known Plaintext attack:** Small amount of plaintext and equivalent ciphertext is known
3. **Chosen Plaintext attack:** Ciphertext equivalent of some plaintext selected by attacker can be obtained.
4. **Chosen Ciphertext attack:** Plaintext equivalent of some ciphertext selected by attacker can be obtained.

## Which attacks should be prevented?

A cryptosystem which can be practically attacked using only ciphertexts is considered highly insecure.

Modern standard is that a cryptosystem should be secure against chosen plaintext and chosen ciphertext attacks.

History shows that chosen ciphertext attacks can often be practical to set up for an attacker.