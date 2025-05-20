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

Simplest k