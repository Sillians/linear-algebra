## **The Gram-Schmidt Process in the General Case**

---

### **1. Overview of the Gram-Schmidt Process**

The **Gram-Schmidt process** is an algorithm for taking a set of **linearly independent vectors** and 
producing an **orthogonal (or orthonormal)** set of vectors that spans the same subspace. 
It is foundational in linear algebra, particularly in constructing orthonormal bases.

#### **Input:**

A set of linearly independent vectors $`{v\_1, v\_2, \dots, v\_n}`$ in an inner product space.

#### **Output:**

An orthogonal set $`{u\_1, u\_2, \dots, u\_n}`$ such that:

* $`\mathrm{span}(v\_1, \dots, v\_n) = \mathrm{span}(u\_1, \dots, u\_n)`$


* Each $`u\_k`$ is orthogonal to all $`u\_j`$ for $`j < k`$

---

### **2. The General Algorithm (Gram-Schmidt Orthogonalization)**

Given:

* $`v\_1, v\_2, \dots, v\_n \in \mathbb{R}^m`$, linearly independent

Construct:

* $`u\_1 = v\_1`$


* $`u\_2 = v\_2 - \mathrm{proj}\_{u\_1}(v\_2)`$


* $`u\_3 = v\_3 - \mathrm{proj}*{u\_1}(v\_3) - \mathrm{proj}*{u\_2}(v\_3)`$


* $`\dots`$


* $`u\_k = v\_k - \sum\_{j=1}^{k-1} \mathrm{proj}\_{u\_j}(v\_k)`$


Where:

$`{\mathrm{proj}_{u_j}(v_k) = \frac{\langle v_k, u_j \rangle}{\langle u_j, u_j \rangle} u_j}`$

To normalize the orthogonal set into an **orthonormal** set:

$`e_k = \frac{u_k}{\|u_k\|}, \quad \text{for } k = 1, 2, \dots, n`$

---

### **3. Finding an Orthogonal Basis of a Span Given Some Orthogonal Vectors**

If a set $`{u\_1, \dots, u\_r}`$ of **orthogonal** vectors is given (i.e., $`\langle u\_i, u\_j \rangle = 0`$ 
for $`i \ne j`$), and the task is to find an orthogonal basis for the span of some larger set 
$`{v\_1, \dots, v\_n}`$ that includes them, proceed by:


1. **Start with the known orthogonal vectors.**


2. **Add other vectors** from the span one at a time.


3. **Apply Gram-Schmidt** to orthogonalize each new vector against the existing orthogonal set.



This guarantees the resulting basis:

* Still spans the original subspace.


* Is fully orthogonal.

---

### **4. Finding an Orthogonal Basis for the Column Space of a Matrix Given Some Orthogonal Columns**

Suppose:

* $`A \in \mathbb{R}^{m \times n}`$ and a subset of its columns $`{a\_1, \dots, a\_k}`$ are orthogonal.

To find an orthogonal basis for $`\mathrm{Col}(A)`$:

1. Begin with the known orthogonal columns.


2. For each remaining column $`a\_j`$, project it onto the subspace spanned by the current orthogonal vectors:


$`\tilde{a}_j = a_j - \sum_{i=1}^{k} \mathrm{proj}_{a_i}(a_j)`$


3. If $`\tilde{a}\_j \ne 0`$, include it in the basis.

Repeat for all remaining columns.

---

### **5. Finding an Orthogonal Basis Using the Gram-Schmidt Process**

Given a matrix $`A = [v\_1 \ v\_2 \ \dots \ v\_n]`$ with linearly independent columns:

* Use Gram-Schmidt to compute orthogonal vectors $`u\_1, u\_2, \dots, u\_n`$


* These form an orthogonal basis for $`\mathrm{Col}(A)`$

#### **Step-by-step summary:**

| Step | Operation                                                                                                    |
| ---- |--------------------------------------------------------------------------------------------------------------|
| 1    | Set $`u\_1 = v\_1`$                                                                                          |
| 2    | For $`k = 2`$ to $`n`$:                                                                                      |
| 3    |  $`u\_k = v\_k - \sum\_{j=1}^{k-1} \frac{\langle v\_k, u\_j \rangle}{\langle u\_j, u\_j \rangle} u\_j`$      |
| 4    | (Optional) Normalize each $`u\_k`$ to get orthonormal vectors $`e\_k = \frac{u\_k}{\|u\_k\|}`$               |

---

### **6. Notes on Stability and Practical Use**

* **Numerical instability** can arise in floating-point arithmetic; the **Modified Gram-Schmidt** (MGS) is often used for better stability.


* In machine learning and data analysis, this is useful for constructing orthonormal feature spaces, QR decompositions, and simplifying projections.

---

### **7. Summary Table**

| Task                     | Given                                   | Goal                              | Method                           |
| ------------------------ | --------------------------------------- |-----------------------------------| -------------------------------- |
| Orthogonalize vector set | Linearly independent $`v\_1, ..., v\_n`$ | Orthogonal basis                  | Apply Gram-Schmidt               |
| Extend orthogonal set    | Some orthogonal vectors, others not     | Orthogonal basis for full span    | Orthogonalize additional vectors |
| Column space basis       | Matrix with orthogonal columns + others | Orthogonal basis for column space | Orthogonalize remaining columns  |
| Orthonormal basis        | Any of the above                        | Orthonormal basis                 | Normalize orthogonal vectors     |

---
