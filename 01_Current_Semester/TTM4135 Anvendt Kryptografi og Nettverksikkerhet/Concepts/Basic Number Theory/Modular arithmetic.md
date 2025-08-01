---
tags:
  - Concept
---
# Concept for [[Basic Number Theory.md]]

$b$ is a residue of $a$ modulo $n$ if $a-b=kn$ for some integer $k$.
$$a\equiv b (\bmod n) <=> a-b=kn$$
## Residue class

A **complete set of residues modulo n** is a set on $n$ integers where every integer is congruendt mod $n$ to exactly one of those numbers.

*For any integer $a$, there ins one nad only one number inthe set that $a \equiv \text{that number} (\bmod n)$*

### Example

$$Z_5 = \{0,1,2,3,4\}$$
for any integer you pick, like $12$, will be congruent to exactly one of these:
$$12 \bmod 5 = 2 \Rightarrow 12 \equiv 2(\bmod 5)$$
So $2$ is the representative of 12 in $Z_5$

## Use

1. Group together "equivalent" numbers:
All numbers congruent mod $n$ (3, 8, 13, 18...) belong to the same **residue class mod $n$**. In mod 5, all of those numbers are congruent to 3:

$$3\equiv8\equiv13\equiv18 (\bmod5)\Rightarrow \text{Belong to residue class of 3}$$
