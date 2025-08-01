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

A group is **cyclic** if it has a **generator**.

The group can be built completely by applying the group operation repeatedly to a single element
## Order of a Group $\left|G\right|$
* Simply **number of elements** in the group $G$

$$Z_6=\{0,1,2,3,4,5\}\rightarrow\left|G\right| = 6$$
**Repeated Application** $g^k$:
* Applying $g$, $k$ times.
$$g^3 = g\times g\times g$$
**Order of an Element $\left| g\right|$**
* the **smallest positive integer $k$** such that
$$g^k = 1$$
**Generator**
* An element $g\in G$ is a **generator** if repeatedly applying it produces all elements of the group
$$\left|g\right| =\left|G\right|$$
# $Z^*_p$

A complete set of residues modulo any prime $p$ with the 0 removed forms a group under multiplication denoted $Z^*_p$.

Some useful properties:
* The order of $Z^*_p$ is $p-1$
* $Z^*_p$ is cyclic
* $Z^*_p$ has many generators in general

$Z^*_p$ can be represented as the multiplicative group of integers $\{1,2, ..., p-1\}$

## Finding a generator of $Z^*_p$

![[{EBB355B2-36C8-4845-84A6-233EE3F9028E}.png]]