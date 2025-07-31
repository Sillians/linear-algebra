## **Jordan Canonical Form of a 3×3 Matrix**

---

### **1. Overview: Jordan Canonical Form (JCF)**

The **Jordan Canonical Form** of a square matrix is a nearly diagonal matrix that reflects both 
the **algebraic** and **geometric** multiplicities of its eigenvalues. It simplifies computations 
involving powers, exponentials, or functions of matrices.

A **Jordan block** for eigenvalue $`\lambda`$ of size $`k`$ is a $`k \times k`$ matrix:

$`J_k(\lambda) = \begin{bmatrix} \lambda & 1 & 0 & \cdots & 0 \\0 & \lambda & 1 & \cdots & 0 \\\vdots & \vdots & \ddots & \ddots & \vdots \\0 & 0 & \cdots & \lambda & 1 \\0 & 0 & \cdots & 0 & \lambda \end{bmatrix}`$

The full **Jordan form** is a block diagonal matrix composed of one or more Jordan blocks.

---

### **2. Finding a Jordan Canonical Form of a 3×3 Matrix With Three Distinct Eigenvalues**

#### **Key Insight**

* If a 3×3 matrix has **three distinct eigenvalues**, then:

  * Each eigenvalue has algebraic and geometric multiplicity of 1.

  * The matrix is **diagonalizable**.

#### **Jordan Form**

$`J = \begin{bmatrix} \lambda_1 & 0 & 0 \\0 & \lambda_2 & 0 \\0 & 0 & \lambda_3 \end{bmatrix}`$

#### **Example**

If eigenvalues are $`2, -1, 4`$, then:

$`J = \begin{bmatrix} 2 & 0 & 0 \\0 & -1 & 0 \\0 & 0 & 4 \end{bmatrix}`$

---

### **3. Finding a Jordan Canonical Form of a 3×3 Matrix With Two Distinct Eigenvalues**

Let’s say the eigenvalues are $`\lambda`$ (multiplicity 2) and $`\mu`$ (multiplicity 1).

#### **Case A: Diagonalizable (Geometric = Algebraic Multiplicity)**

If both eigenvalues have geometric multiplicities equal to their algebraic multiplicities, then:


$`J = \begin{bmatrix} \lambda & 0 & 0 \\0 & \lambda & 0 \\0 & 0 & \mu \end{bmatrix}`$


#### **Case B: Non-diagonalizable**

Suppose geometric multiplicity of $`\lambda`$ is 1 (not equal to algebraic multiplicity 2). Then:

* One Jordan block of size 2 for $`\lambda`$


* One 1×1 block for $`\mu`$


$`J = \begin{bmatrix} \lambda & 1 & 0 \\0 & \lambda & 0 \\0 & 0 & \mu \end{bmatrix}`$


#### **Example**

For eigenvalues $`\lambda = 3`$ (mult. 2), $`\mu = 1`$:

* If diagonalizable:

$`J = \begin{bmatrix} 3 & 0 & 0 \\0 & 3 & 0 \\0 & 0 & 1 \end{bmatrix}`$

* If not diagonalizable:

$`J = \begin{bmatrix} 3 & 1 & 0 \\0 & 3 & 0 \\0 & 0 & 1 \end{bmatrix}`$

---

### **4. Finding a Jordan Canonical Form of a 3×3 Matrix With Only One Eigenvalue**

Let eigenvalue $`\lambda`$ have algebraic multiplicity 3.

#### **Case A: Diagonalizable**

Geometric multiplicity = 3:

$`J = \begin{bmatrix} \lambda & 0 & 0 \\0 & \lambda & 0 \\0 & 0 & \lambda \end{bmatrix}`$

#### **Case B: One Jordan Block of Size 2 and One of Size 1**

Geometric multiplicity = 2:

$`J = \begin{bmatrix} \lambda & 1 & 0 \\0 & \lambda & 0 \\0 & 0 & \lambda \end{bmatrix}`$

#### **Case C: One Jordan Block of Size 3**

Geometric multiplicity = 1:

$`J = \begin{bmatrix} \lambda & 1 & 0 \\0 & \lambda & 1 \\0 & 0 & \lambda \end{bmatrix}`$

#### **Example**

For eigenvalue $`-4`$:

* If diagonalizable:

$`J = \begin{bmatrix} -4 & 0 & 0 \\0 & -4 & 0 \\0 & 0 & -4 \end{bmatrix}`$

* If geometric mult. = 2:

$`J = \begin{bmatrix} -4 & 1 & 0 \\0 & -4 & 0 \\0 & 0 & -4 \end{bmatrix}`$

* If geometric mult. = 1:

$`J = \begin{bmatrix} -4 & 1 & 0 \\0 & -4 & 1 \\0 & 0 & -4 \end{bmatrix}`$

---

### **Summary Table: Jordan Form Patterns for 3×3 Matrices**

| Case                          | Eigenvalue(s)                       | Algebraic Multiplicities | Geometric Multiplicities | Jordan Form                  |
| ----------------------------- |-------------------------------------| ------------------------ | ------------------------ | ---------------------------- |
| All distinct                  | $`\lambda_1, \lambda_2, \lambda_3`$ | 1, 1, 1                  | 1, 1, 1                  | Diagonal                     |
| Two equal                     | $`\lambda, \lambda, \mu`$           | 2, 1                     | 2, 1                     | Diagonal                     |
| Two equal, non-diagonalizable | $`\lambda, \lambda, \mu`$           | 2, 1                     | 1, 1                     | One block size 2             |
| One eigenvalue                | $`\lambda`$                         | 3                        | 3                        | Diagonal                     |
| One eigenvalue                | $`\lambda`$                         | 3                        | 2                        | One block size 2, one size 1 |
| One eigenvalue                | $`\lambda`$                         | 3                        | 1                        | One block size 3             |

---
