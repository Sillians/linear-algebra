## **Jordan Blocks and Jordan Matrices**

---

### **1. What Is a Jordan Block?**

A **Jordan block** is a special kind of square matrix used in **Jordan canonical form**. 
It represents the structure of a **non-diagonalizable matrix** or one with **repeated eigenvalues** and **defective eigenspaces**.

A **Jordan block** corresponding to an eigenvalue $`\lambda`$ of size $`n \times n`$ is defined as:

$`J_n(\lambda) = \begin{bmatrix} \lambda & 1 & 0 & \cdots & 0 \\0 & \lambda & 1 & \cdots & 0 \\0 & 0 & \lambda & \cdots & 0 \\\vdots & \vdots & \vdots & \ddots & 1 \\0 & 0 & 0 & \cdots & \lambda \end{bmatrix}`$

* **Diagonal**: All entries are $`\lambda`$


* **Superdiagonal**: All entries immediately above the diagonal are 1


* **Zero elsewhere**

---

### **2. Identifying Jordan Blocks**

A matrix is a **Jordan block** if:

* All diagonal entries are equal to a scalar $`\lambda`$


* All superdiagonal entries are 1


* All other entries are 0


**Examples:**

* $`J_1(5) = [5]`$


* $`J_2(3) = \begin{bmatrix} 3 & 1 \\ 0 & 3 \end{bmatrix}`$


* $`J_3(-2) = \begin{bmatrix} -2 & 1 & 0 \\ 0 & -2 & 1 \\ 0 & 0 & -2 \end{bmatrix}`$

---

### **3. Constructing Jordan Blocks**

To construct a Jordan block:

1. Choose an eigenvalue $`\lambda`$


2. Choose a size $n$


3. Fill the matrix such that:

   * Diagonal is $`\lambda`$
   * Superdiagonal is 1
   * All else is 0

$`J_n(\lambda) = \lambda I_n + N`$

Where $N$ is a **nilpotent matrix** with ones on the superdiagonal.

---

### **4. Jordan Matrices: Compositions of Jordan Blocks**

A **Jordan matrix** is a **block diagonal matrix** with **Jordan blocks** on the diagonal.

**Example:**

$`J = \begin{bmatrix} J_2(3) & 0 \\0 & J_1(2)\end{bmatrix}= \begin{bmatrix} 3 & 1 & 0 \\0 & 3 & 0 \\0 & 0 & 2 \end{bmatrix}`$

This represents a matrix with:

* Eigenvalue 3 of algebraic multiplicity 2


* Eigenvalue 2 of algebraic multiplicity 1

---

### **5. Identifying a Matrix as a Composition of Jordan Blocks**

Given a matrix $A$, to determine if it corresponds to a Jordan matrix:

1. **Find its eigenvalues** (roots of characteristic polynomial).


2. **Check algebraic and geometric multiplicities**:

   * If algebraic > geometric multiplicity, matrix is **not diagonalizable**, but has a Jordan form.


3. Determine the size and number of Jordan blocks by:

   * **Size** of each block from the **chains of generalized eigenvectors**
   * **Number** of blocks equals **dimension of eigenspace**

---

### **6. Writing a Matrix as a Composition of Jordan Blocks**

The **Jordan form** of a matrix $A$ is:

$`J = P^{-1} A P`$

Where:

* $J$ is a block diagonal matrix of Jordan blocks


* $P$ contains **generalized eigenvectors**



To write $A$ as a composition of Jordan blocks:

1. Find eigenvalues $`\lambda`$


2. Compute **nullities** of $`(A - \lambda I)^k`$ for increasing $k$


3. Determine block sizes


4. Form $J$ as a block diagonal matrix

---

### ✅ Summary Table

| Concept                   | Description                                                            |
| ------------------------- | ---------------------------------------------------------------------- |
| **Jordan Block**          | Upper-triangular matrix with eigenvalue $`\lambda`$, ones above diagonal |
| **Jordan Matrix**         | Block diagonal matrix of Jordan blocks                                 |
| **Diagonalizable matrix** | All Jordan blocks are 1×1                                              |
| **Defective matrix**      | At least one Jordan block is larger than 1×1                           |
| **Nilpotent part**        | Off-diagonal structure showing failure to diagonalize                  |
| **Jordan Canonical Form** | Simplifies study of linear transformations with repeated eigenvalues   |

---

### **Applications**

* Jordan form helps solve systems of differential equations


* Reveals structure of linear transformations


* Fundamental in understanding similarity, minimal polynomials, and matrix exponentials

