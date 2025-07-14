## **Introduction to Abstract Vector Spaces**

---

### **Overview**

An **abstract vector space** is a set $`V`$ equipped with two operations:

1. **Vector addition**: $`+ : V \times V \rightarrow V`$


2. **Scalar multiplication**: $`\cdot : \mathbb{F} \times V \rightarrow V`$

where $`\mathbb{F}`$ is a field (typically $`\mathbb{R}`$ or $`\mathbb{C}`$), satisfying a set of 
axioms (e.g., associativity, distributivity, existence of additive identity, etc.).

---

### **1. Identifying Sets Closed Under Addition and Scalar Multiplication**

To verify that a set is a **vector space**, we often first check **closure**:

* **Addition**: For all $`u, v \in V`$, we require $`u + v \in V`$.
* **Scalar multiplication**: For all $`v \in V`$ and $`c \in \mathbb{F}`$, we require $`c \cdot v \in V`$.

**Example**:
Let $`V = \{(x, y) \in \mathbb{R}^2 : x + y = 0\}`$
Check closure:

* $`(x_1 + y_1 = 0)`$ and $`(x_2 + y_2 = 0)`$

* Then $`(x_1 + x_2) + (y_1 + y_2) = (x_1 + y_1) + (x_2 + y_2) = 0 + 0 = 0 \Rightarrow`$ closed under addition.


* Similarly, $`c(x, y) = (cx, cy)`$ → $`cx + cy = c(x + y) = c(0) = 0 \Rightarrow`$ closed under scalar multiplication.

✅ Hence, it is a subspace (a vector space).

---

### **2. Verifying Properties Involving Vector Addition**

For all $`u, v, w \in V`$, check:

* **Commutativity**: $`u + v = v + u`$


* **Associativity**: $`(u + v) + w = u + (v + w)`$


* **Additive identity**: There exists $`0 \in V`$ such that $`v + 0 = v`$


* **Additive inverse**: For all $`v \in V`$, there exists $`-v \in V`$ such that $`v + (-v) = 0`$

These properties ensure the **additive group structure** of the vector space.

---

### **3. Verifying Properties Involving Scalar Multiplication and the Distributive Laws**

For all $`a, b \in \mathbb{F}`$, $`u, v \in V`$, check:

* **Distributivity over vector addition**:
  $`a(u + v) = au + av`$


* **Distributivity over scalar addition**:
  $`(a + b)u = au + bu`$


* **Associativity of scalar multiplication**:
  $`a(bu) = (ab)u`$


* **Identity scalar**:
  $`1 \cdot u = u`$

These are crucial to verify the **module structure** over the field $`\mathbb{F}`$.

---

### **Summary**

A set becomes a **vector space** over a field $`\mathbb{F}`$ if:

* It is closed under addition and scalar multiplication.


* All 8 vector space axioms are satisfied.

Understanding and verifying **closure and distributive/associative properties** is foundational for 
studying **abstract linear algebra** and proofs within more general vector spaces.
