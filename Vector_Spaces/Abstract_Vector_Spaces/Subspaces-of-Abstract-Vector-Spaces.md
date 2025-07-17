## **Subspaces of Abstract Vector Spaces**

---

### **1. Overview of Abstract Vector Spaces**

An **abstract vector space** is a set of elements (vectors) along with two operations (vector addition and scalar multiplication) satisfying axioms like associativity, 
distributivity, existence of a zero vector, and additive inverses. Common examples:

* ℝⁿ (real coordinate spaces),


* Function spaces (like all continuous functions),


* Polynomial spaces (like all polynomials of degree ≤ n),


* Matrix spaces (like all 2×2 matrices over ℝ or ℂ).

---

### **2. What Is a Subspace?**

A **subspace** of a vector space is a subset that is itself a vector space under the same operations. 
For a subset $`W \subseteq V`$ to be a subspace, it must satisfy:

1. **Zero Vector**: $`0 \in W`$


2. **Closed under Addition**: If $`u, v \in W`$, then $`u + v \in W`$


3. **Closed under Scalar Multiplication**: If $`u \in W`$ and $`c \in \mathbb{F}`$, then $`cu \in W`$

---

### **3. Identifying Subspaces of Polynomial Vector Spaces**

Let $`P\_n`$ be the vector space of all real polynomials of degree at most $`n`$.

**Examples of subspaces:**

* The set of all polynomials in $`P\_n`$ with even powers only:
  $`W = \{ a_0 + a_2x^2 + a_4x^4 + \dots \mid a_i \in \mathbb{R} \}`$
  ✅ Contains 0, closed under addition and scalar multiplication.


* The set of all polynomials $`p(x) \in P\_3`$ such that $`p(1) = 0`$
  ✅ This defines a **kernel** of the evaluation functional at $`x=1`$, hence a subspace.


**Non-example:**

* Set of all polynomials in $`P\_2`$ with degree exactly 2
  ❌ Not closed under addition (sum of two degree-2 polynomials might be lower degree).

---

### **4. Identifying Subspaces of Matrix Vector Spaces**

Let $`M\_{m \times n}`$ be the space of all $`m \times n`$ matrices.

**Examples of subspaces:**

* The set of all **symmetric** $`n \times n`$ matrices: $`A = A^T`$
  ✅ Closed under addition and scalar multiplication.



* The set of all **upper triangular** matrices in $`M\_{n \times n}`$
  ✅ Closed under addition and scalar multiplication.



**Non-example:**

* The set of all invertible matrices
  ❌ Not closed under scalar multiplication (e.g., scaling by 0 gives a non-invertible matrix).

---

### **5. Identifying Subspaces of Function Vector Spaces**

Let $`F`$ be the space of all real-valued functions defined on ℝ.

**Examples of subspaces:**

* The set of **continuous functions**: $`C(\mathbb{R})`$
  ✅ Addition and scalar multiples of continuous functions are still continuous.



* The set of functions $f$ such that $`f(0) = 0`$
  ✅ Contains zero function, closed under both operations.



* The set of **even functions**: $`f(-x) = f(x)`$
  ✅ Subspace.



**Non-example:**

* The set of all functions with value 1 at $`x=0`$
  ❌ Not closed under scalar multiplication (e.g., scaling a function that satisfies $`f(0) = 1`$ by 2 gives $`f(0) = 2`$).

---

### **Summary Table**

| Vector Space Type            | Example Subspace                 | Why It’s a Subspace                           |
|------------------------------|----------------------------------| --------------------------------------------- |
| Polynomial ($`P\_n`$)        | $`{ p \in P\_n \mid p(1) = 0 }`$ | Zero included, closed under operations        |
| Matrix ($`M\_{n \times n}`$) | Symmetric matrices               | Preserved under sum and scalar multiplication |
| Function ($`f: ℝ \to ℝ`$)    | $f$ s.t. $`f(0) = 0`$            | Satisfies all subspace conditions             |

---

### **Geometric Insight**

Subspaces behave like **"flat" structures** (lines, planes, hyperplanes) through the origin in their 
respective spaces. They are the "directions" a vector space can move without breaking the linear structure.
