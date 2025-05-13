---
tags:
  - Concept
---
# Concept for [[Basic Number Theory.md]]

Inverse of $a$, if exists, is a value $x$ such that
$$ax=1(\bmod n)$$
and is written $a^-1 \bmod n$

Needed in cryptosystems to find inverses so that we can decrypt, or undo certain operations.

$a$ has an inverse modulo $n$ if and only if $gcd(a,n) = 1\text{ and } 0<a<n$

## Modular inverses using Euclidean algorithm

We want to solve $x$ given $a$:
$$ax\equiv 1 (\bmod n)$$
Using the extended Euclidean Algorithm:
$$a\cdot x + n \cdot y = 1$$
