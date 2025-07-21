## **Jordan Canonical Form of a 2x2 Matrix**

---

### **Overview of the Jordan Canonical Form (JCF)**

The **Jordan Canonical Form (JCF)** of a matrix is a block diagonal matrix that reveals the geometric and algebraic multiplicities of eigenvalues. 
For a square matrix $`A`$, the JCF simplifies $`A`$ into a matrix $`J`$ such that:


$`A = PJP^{-1}`$


where $`P`$ is the matrix of (generalized) eigenvectors and $`J`$ has Jordan blocks on its diagonal.


For **2x2 matrices**, JCF takes one of the following forms:


1. **Diagonal matrix** if there are two distinct eigenvalues.


2. **Scalar matrix** if all entries are the same scalar multiple of the identity.


3. **Single Jordan block** if there is only one eigenvalue and the matrix is not diagonalizable.

---

### **Finding a Jordan Canonical Form of a 2x2 Matrix With Two Distinct Eigenvalues**

Let $`A = \begin{bmatrix} a & b \ c & d \end{bmatrix}`$.

1. Compute the **characteristic polynomial**:


$`\det(A - \lambda I) = \lambda^2 - \mathrm{tr}(A)\lambda + \det(A)`$


2. If it has **two distinct eigenvalues** $`\lambda\_1 \ne \lambda\_2`$, then $`A`$ is diagonalizable:


$`J = \begin{bmatrix} \lambda_1 & 0 \\0 & \lambda_2 \end{bmatrix}`$


3. Find corresponding linearly independent eigenvectors to form $`P`$.

---

### **Finding a Jordan Canonical Form of a 2x2 Scalar Matrix**

A scalar matrix is of the form:


$`A = \lambda I = \begin{bmatrix} \lambda & 0 \\0 & \lambda \end{bmatrix}`$


Its Jordan form is trivially itself:


$`J = \begin{bmatrix} \lambda & 0 \\0 & \lambda \end{bmatrix}`$


This is diagonal and already in JCF with both eigenvalues equal to $`\lambda`$ and algebraic multiplicity 2.

---

### **Finding a Jordan Canonical Form of a 2x2 Matrix With Only One Eigenvalue**

Let $A$ have a **single eigenvalue** $`\lambda`$ with **algebraic multiplicity 2** but **geometric multiplicity 1** (i.e., only one linearly independent eigenvector).


Then $`A`$ is **not diagonalizable**, and the JCF has a single Jordan block:


$`J = \begin{bmatrix} \lambda & 1 \\0 & \lambda \end{bmatrix}`$


To find it:


1. Compute the characteristic polynomial and solve for the eigenvalue.


2. Check that there is only **one linearly independent eigenvector** (null space of $`A - \lambda I`$ is 1D).


3. Find a **generalized eigenvector** $v$ such that $`(A - \lambda I)^2 v = 0`$, but $`(A - \lambda I) v \ne 0`$.


4. Use eigenvector and generalized eigenvector to form $`P`$ such that $`A = PJP^{-1}`$.

---

### **Summary Table**

| Matrix Type                        | Eigenvalues                        | Jordan Canonical Form                                             |
| ---------------------------------- |------------------------------------|-------------------------------------------------------------------|
| Two distinct eigenvalues           | $`\lambda\_1 \ne \lambda\_2`$      | $`\begin{bmatrix} \lambda\_1 & 0 \ 0 & \lambda\_2 \end{bmatrix}`$ |
| Scalar matrix                      | $`\lambda = \lambda`$              | $`\begin{bmatrix} \lambda & 0 \ 0 & \lambda \end{bmatrix}`$       |
| One eigenvalue, not diagonalizable | $`\lambda`$ (only one eigenvector) | $`\begin{bmatrix} \lambda & 1 \ 0 & \lambda \end{bmatrix}`$       |

---

