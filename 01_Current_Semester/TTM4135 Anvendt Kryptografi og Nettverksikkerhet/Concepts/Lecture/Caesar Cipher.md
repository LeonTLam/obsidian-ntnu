---
tags:
  - Concept
---
# Concept for [[Week_1 Lecture 3 Classical Encryption]]

*Technique which involves shifting the letters of the alphabet by a fixed number of places.*

## Cryptography Algorithm

To cipher plain-text using Caesar Cipher, we need a **shift** integer which indicates the number of positions each letter of the text will be moved.

To decrypt a cipher-text using Caesar Cipher, we simply shift each letter back by the same number of positions.

## Advantages

* Not secure against modern decryption methods.
* Vulnerable to known-plaintext attacks, where the **attacker** knows both the encrypted and nonencrypted versions of the same message.
* Small number of keys implies that an attacker can easily brute-force all possible keys.
* Not suitable for long text encryption.
* Not suitable for secure communication, easily broken.
* Does not provide [[Confidentiality]], [[Integrity]], and [[authenticity]] in a message.

## Breaking a Caesar Cipher
### Encryption
$C = (P+k)\mod 26$
Where $C$ is the ciphertext, $P$ is the plaintext, and $k$ is the key (shift value)
### Decryption
$P = (C-k) \mod26$

### Key Methods

Since there are only 25 possible keys (shifts), you can try all and look for meaningful plaintext.

Comparing the frequency of letters in the ciphertext, to the known frequency of letters in the language ("E" being the most common letter in English)