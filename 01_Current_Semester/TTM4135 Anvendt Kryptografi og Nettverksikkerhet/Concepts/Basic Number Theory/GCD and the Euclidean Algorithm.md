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

Method to compute **greatest common divisor** of two integers $a$ and $b$, where $a > b$


**Task 1:**
$gcd(198,126)$

$$ \begin{aligned}
198 = 126 * 1 + 72 \\
126 = 72*1+54 \\ 
72 = 54*1+18 \\
54= 18*3+0 \\
gcd(198,126)=18
\end{aligned}$$
**Task 2:**
$gcd(391,299)$

$$\begin{aligned}
391 = 299*1+92\\
299= 92*3+23\\
92 = 23*4+0
gcd(391,299)=23
\end{aligned}$$
**Task 3:**
$gcd(867,255)$
$$\begin{aligned}
867 = 255*3+102 \\
255 = 102*2+51 \\
102 = 51*2+0
gcd(867,299)=51
\end{aligned}$$

### Back Substitution (Extended Euclidean Algorithm)

Method used in the **extended Euclidean algorithm** to express GCD of two integers $a$ and $b$ as linear combination

$$\begin{aligned}
gcd(a,b) = ax+by
\end{aligned}$$
Where $x$ and $y$ are integers. Useful in number theory and cryptography.

#### Step-by-step
1. Use Euclidean algorithm to compute the GCD
2. Once hit remainder 0, go one step back
3. Substitute repeatedly
	1. Rebuild expressions until you write GCD as combination of the original $a$ and $b$

**Task 1:**
$gcd(198,126)=198x+126y$

$$\begin{aligned}
\end{ali}