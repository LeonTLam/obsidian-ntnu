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

$$ \begin{aligned}
198 = 126 * 1 + 72 \\
72 = 36*2+0 \\ 
gcd(198,126)=36
\end{aligned}$$
**Task 2:**
$gcd(391,299)$

$$\begin{aligned}
391 = 299*1+92\\
92= 46*2=0\\
gcd(391,299)=46
\end{aligned}$$
**Task 3:**
$gcd(867,299)$
$$\begin{aligned}
867 = 299*2+269\\
269=
\end{aligned}$$

