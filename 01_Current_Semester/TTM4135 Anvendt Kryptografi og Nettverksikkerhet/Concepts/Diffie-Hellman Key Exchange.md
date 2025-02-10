---
tags:
  - Concept
---
# Concept for [[Week_5 Discrete Log Public Key Cryptosystems.md]]

## Example
* Two users share secret using only public communication.
* Public knowledge: Generator g of a multiplicative group G of order t.
* Both users each select random values 'a' and 'b' where 0<a, b<t.
* Alice sends $g^a$ to Bob (over insecure channel)
* Bob sends $g^b$ to Alice
* Both users compute secret key $Z = g^{ab}$
* Originally group G used was $Z^*_p$ for large p

## Example in $Z^*_p$ 
Public knowledge is $p = 181, g =2$
* Alice selects $a=50$
* Bob selects $b=33$

* Alice sends $g^50\mod181 = 116$ to Bob
* Bob sends $g^33 \mod 181 = 30$ to Alice