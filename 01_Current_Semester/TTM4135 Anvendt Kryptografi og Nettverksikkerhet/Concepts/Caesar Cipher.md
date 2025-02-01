---
tags:
  - Concept
---
# Concept for [[Week_1 Lecture 3 Classical Encryption.md]]

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
