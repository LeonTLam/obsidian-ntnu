# 27-Jan-2025 Daily Note for [[TTM4135]]

## Topics Covered
- Chinese Remainder Theorem
- Topic 2

---
## Key Points

# Chinese Remainder Theorem

```Example
x == 5 (mod 6)
x == 33 (mod 35)
1. Check if both "mod X's" are co-primes (GCD)
2. n = x_1 * x_2
3. d_1 = 6, d_2 = 35, n = 6 * 35 = 210
4. c_1 = 5, c_2 = 33

1.y_i == (n / d_1)^-1 (mod d_i)
2.(n / d_1)y_i === 1 (mod 6)
3.210/6 y_i === 1 (mod 6)
4.30 y_i === 1 (mod 6)
5. 5y_i === 1 (mod 6)
6. gcd(5,6)=1, 5 has an inverse mod 6
7. 1 = 6 * 1 - 1 * 5, Euclidean Algorithm
8. 5^-1 == -1 == 5 (mod 6)

y_1 == 5 (mod 6)

y_2 
```


---
## Notes
- Additional notes or reminders.

---

Created on 27-Jan-2025 12:21
