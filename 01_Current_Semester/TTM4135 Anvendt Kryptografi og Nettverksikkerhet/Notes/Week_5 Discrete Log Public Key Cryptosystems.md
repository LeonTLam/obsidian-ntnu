# 10-Feb-2025 Daily Note for [[TTM4135]]

## Topics Covered
- Diffie-Hellman Key Exchange
	- Protocol
	- Properties
- Elgamal Cryptosystem
	- Algorithm
	- Security
- Elliptic Curves
- Elliptic Curve Cryptography
- Post-Quantum Cryptography

---
## Key Points

# Diffie-Hellman Key Exchange

* Two users share secret using only public communication.
* Public knowledge: Generator g of a multiplicative group G of order t.
* Both users each select random values 'a' and 'b' where 0<a, b<t.
* Alice sends $g^a$ to Bob (over insecure channel)
* Bob sends $g^b$ to Alice
* Both users compute secret key $Z = g^{ab}$
* Originally group G used was $Z^*_p$ for large p


---
## Notes
- Additional notes or reminders.

---

Created on 10-Feb-2025 15:03
