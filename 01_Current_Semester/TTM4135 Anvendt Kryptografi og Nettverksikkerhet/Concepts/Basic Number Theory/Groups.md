---
tags:
  - Concept
---
# Concept for [[Basic Number Theory.md]]

A **group** is a set of $G$, with a binary operation $\cdot$ , satisfying following conditions 
![[{0584840C-E456-44C1-BC49-A860F7B70051}.png]]
## Definition "Abelian group"

*a group in which the result of applying the group operation to two group elements does not depend on the order in which they are written*

### Example

Check if ($Z$, $+$) forms a group:
$Z = \{-3,-2,-1,0,1,2,3\}$

**Closure:**
Add any two integers, you get another integer
$$3+-5 = -2 \in Z\text{ or }-5+3=-2\in Z$$
**Identity:**
Identity element is $0$, because
$$a+0=0+a=a\text{ for any } a\in Z$$
**Inverse:**
Each integer has an additive inverse:
$$\text{For }a = 7\text{ inverse is }-7 \text{ ,since } 7+(-7) = 0$$
**Associativity:**
Addition of integers is associative
$$(a+b)+c=a+(b+c)$$
**Commutativity:**
Addition is commutative
$$a+b=b+a$$
**Conclusion:**
$(Z, +)$ is an **abelian group**.

# Cyclic groups

## Order of a Group $\left|G\right|$
* Simply **number of elements** in the group $G$

$$Z_6=\{0,1,2,3,4,5\}\rightarrow\left|G\right| = 6$$
**Repeated Application** $g^k$:
* Applying $g$, $k$ times.
$$g^3 = g\times g\times g$$