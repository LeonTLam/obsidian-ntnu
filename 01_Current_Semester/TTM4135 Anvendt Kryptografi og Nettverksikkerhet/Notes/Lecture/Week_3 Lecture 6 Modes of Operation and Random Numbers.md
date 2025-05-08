# 20-Jan-2025 Daily Note for [[TTM4135]]

## Topics Covered
- Block Ciphers
- Random numbers
- Using Block Ciphers to generate Random numbers

---
## Key Points
# Purpose of different Modes

Designed to provide confidentiality for data, or to provide authentication (and integrity) for data or to provide both.

We focus on **confidentiality** modes which normally include **randomisation**

Some modes can be used to generate pseudorandom numbers

Different modes have different efficiency or communication properties.

# Importance of randomised encryption

There will be patterns in ciphertext block where same plaintext block is used every time.

Use randomised encryption schemes to prevent this

Typically achieved using *initialisation vector, UV*, which propagates through the entire cipher text. IV may need to be unique and/or random.

Another way to vary, include variable state

## Efficiency

Important features of different modes, does not impact security:
	Some modes allow parallel processing
		Sometimes multiple plaintext blocks can be encrypted in parallel
		Sometimes multiple ciphertext blocks can be decrypted in parallel

## Padding

Some modes, ECB and CBC require the plaintext to consist of one or more complete blocks.

NIST special Publication suggest:
	1. append a single '1' bit to the data string
	2. pad the resulting string by as few '0' bits, possibly none, as are necessary to complete the final block

Padding bits can be removed unambiguously, if receiver knows that this padding method is used.
	1. Remove all trailing '0' bits after the last '1' bit
	2. remove single '1' bit.
Alternative, Cipher Stealing



---
## Notes
- Additional notes or reminders.

---

Created on 20-Jan-2025 12:16
