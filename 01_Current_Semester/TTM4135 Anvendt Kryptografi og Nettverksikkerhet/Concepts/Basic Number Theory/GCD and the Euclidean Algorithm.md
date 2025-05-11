---
tags:
  - Concept
---
# Concept for [[Basic Number Theory.md]]

Value $d$ = $GCD$ of $a$ and $b$, written $gcd(a,b) = d$, IF ALL FOLLOWING HOLD`:

1. $d$ divides $a$ and $b$
``` Example
d|a and d|b

a = d*k and b = d*l
```
2. if $c$ divides $a$ and $b$ then $c$ divides $d$
``` Example
if c|a and c|b, then c|d

c må ha en fellesfaktor til a, så b, så d
```
3. d > 0
``` Forklaring
d må altså være større enn 0, hvis det skal regnes som felles divisor, alt kan jo deles på 0...
```

## Euclidean Algorithm

**Task 1:**
$gcd(198,126)$

$198 = 126*1+72 $