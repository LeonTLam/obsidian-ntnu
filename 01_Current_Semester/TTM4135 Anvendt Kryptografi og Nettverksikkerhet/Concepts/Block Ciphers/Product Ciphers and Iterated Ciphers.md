---
tags:
  - Concept
---
# Concept for [[Block Ciphers.md]]

## Product Cipher
A product cipher is a cryptosystem in which encryption function is formed by applying several sub-encryption functions
Most block ciphers are the composition of simple functions $f_i$ for $i=1,...,r$ where each $f_i$ has a different key $K_i$.

$$C=E(P,K)=f_r(...(f_2(f_1(P,K_1),K_2)...),K_r)$$
## Iterated Cipher
Most modern blocks ciphers are in special class of product ciphers known as **iterated ciphers**.
* Encryption process divided into $r$ similar **rounds**.
* Sub-encryption functions are all same function, $g$, called **round function**.
* Each key $K_i$ derived from overall master key $K$. The keys $K_i$ are called **round keys** or **subkeys** and are derived from $K$ using a process called **key schedule**.
