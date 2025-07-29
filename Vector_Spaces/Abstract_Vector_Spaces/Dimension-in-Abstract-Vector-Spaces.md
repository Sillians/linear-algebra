## **Dimension in Abstract Vector Spaces**

---

### **1. What is Dimension in Abstract Vector Spaces?**

#### **Definition**

The **dimension** of a vector space $`V`$, denoted $`\dim(V)`$, is the number of vectors in a **basis** of $V$, where a **basis** is a set of vectors that:


* **Span** the space: every vector in $V$ can be written as a linear combination of them,


* Are **linearly independent**.

If such a basis is finite, the space is **finite-dimensional**; otherwise, it is **infinite-dimensional**.

---

### **2. Determining the Dimension of a Polynomial Vector Space Given Its Standard Monomial Basis**

Let $`\mathbb{P}_n`$ be the vector space of all real polynomials of degree **at most** $n$.

#### **Standard Monomial Basis**

$`\mathcal{B} = \{1, x, x^2, \ldots, x^n\}`$

This basis contains $`n + 1`$ vectors.

#### **Dimension**

$`\dim(\mathbb{P}_n) = n + 1`$

#### **Example**

For $`\mathbb{P}_3`$:

$`\mathcal{B} = \{1, x, x^2, x^3\} \Rightarrow \dim(\mathbb{P}_3) = 4`$

---

### **3. Determining the Dimension of a Matrix Vector Space Given Its Standard Basis**

Let $`M_{m \times n}(\mathbb{R})`$ be the space of all $`m \times n`$ real matrices.

#### **Standard Basis**

This consists of matrices $`E_{ij}`$ where:

* $`E_{ij}`$ has a 1 in position $`(i,j)`$,


* All other entries are 0.


There are $`m \cdot n`$ such matrices.

#### **Dimension**


$`\dim(M_{m \times n}) = m \cdot n`$

#### **Example**

For $`M_{2 \times 3}(\mathbb{R})`$:


$`\dim(M_{2 \times 3}) = 2 \cdot 3 = 6`$

---

### **4. Identifying True Statements About Dimensions of Vector Spaces**

| Statement                                                                                       | Truth Value | Explanation                                                          |
| ----------------------------------------------------------------------------------------------- | ----------- | -------------------------------------------------------------------- |
| Every basis of a finite-dimensional vector space has the same number of elements.               | ✅ True      | This number defines the dimension.                                   |
| The zero vector space has dimension 0.                                                          | ✅ True      | It contains only the zero vector and no basis.                       |
| A set with more vectors than the dimension of the space is always linearly dependent.           | ✅ True      | Maximum number of linearly independent vectors equals the dimension. |
| A set of linearly independent vectors in a finite-dimensional space can be extended to a basis. | ✅ True      | Fundamental theorem of finite-dimensional vector spaces.             |
| A vector space of infinite dimension can have a finite basis.                                   | ❌ False     | Infinite-dimensional spaces cannot have finite bases.                |

---

### **5. Identifying Finite and Infinite-Dimensional Vector Spaces**

| Vector Space                                           | Dimension     | Finite or Infinite |
|--------------------------------------------------------|---------------| ------------------ |
| $`\mathbb{R}^n`$                                       | $`n`$         | Finite             |
| $`\mathbb{P}_n`$ (polynomials of degree ≤ $`n`$)         | $`n + 1`$     | Finite             |
| $`M_{m \times n}(\mathbb{R})`$                         | $`m \cdot n`$ | Finite             |
| $`\mathbb{P}`$ (all real polynomials, no degree bound) | Infinite      | Infinite           |
| $`C[0, 1]`$ (continuous functions on $`[0,1]`$)        | Infinite      | Infinite           |

#### **Explanation**

* $`\mathbb{P}_n`$, $`\mathbb{R}^n`$, and $`M_{m \times n}`$ have finite bases.


* $`\mathbb{P}`$, $`C[0,1]`$, $`\mathbb{R}^\mathbb{N}`$ are **infinite-dimensional**, since no finite set can span the space.

---

### **Summary Table**

| Concept                  | Key Insight                         |
|--------------------------|-------------------------------------|
| Dimension                | Number of vectors in a basis        |
| Finite-dimensional       | Has a finite basis                  |
| Infinite-dimensional     | No finite spanning set              |
| $`\dim(\mathbb{P}_n)`$   | $`n + 1`$                           |
| $`\dim(M_{m \times n})`$ | $`m \cdot n`$                       |
| Basis size               | Same for any basis of a given space |

---
