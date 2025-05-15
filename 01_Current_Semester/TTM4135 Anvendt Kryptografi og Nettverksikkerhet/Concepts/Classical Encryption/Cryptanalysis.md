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