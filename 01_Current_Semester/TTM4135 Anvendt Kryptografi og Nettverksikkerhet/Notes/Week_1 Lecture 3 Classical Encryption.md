# 13-Jan-2025 Daily Note for [[TTM4135 Week_1 Lecture 3 Classical Encryption]]

## Topics Covered
- Introduction
	- Basic definitions
	- Cryptanalysis
	- Statistics of Natural Language
- Transposition Ciphers
- Simple Substitution Ciphers
	- Caesar Cipher
	- Random Simple Substitution Cipher
- Polyalphabetic Substitution
	- Vignenère Cipher
	- Other Polyalphabetic Ciphers

---
## Key Points

# Introduction

* Cryptography - *the study of designing cryptosystems*
* Cryptanalysis - *the study of breaking cryptosystems*
Both studied together in practice

## Confidentiality and Authentication

* Cryptography - *secret writing*, transformation of data depending on secret called **key**
	* Can be used to provide *confidentiality* and to provide *authentication (or integrity)*
	* When used for conf., a key is required to read.
	* When used for auth., a key required to write

## Cryptosystems

A cryptosystem consists of:
* Set of plaintexts (original message)
* Set of ciphertexts (encrypted message)
* Set of keys 
* function to transform plaintext into ciphertext 
* Inverse to transform ciphertext to plaintext (decryption)

## Symmetric and asymmetric cryptography 

* Symmetric Key Cipher (secret key cipher)
	* Encryption and decryption keys known only to sender and receiver
	* Requires secure channel for transmission of the cryptographic key
* Asymmetric Key Cipher (public key cipher)
	* Each participant has a public key and a private key
	* May allow for both encryption and creation of digital signatures
	* Public key ciphers will be studied later

---
## Notes
- Additional notes or reminders.

---

Created on 13-Jan-2025 16:27
