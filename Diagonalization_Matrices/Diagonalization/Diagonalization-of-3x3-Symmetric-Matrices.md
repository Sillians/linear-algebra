# **Diagonalization of 3×3 Symmetric Matrices**

---

## **1. Overview**

Any **real symmetric matrix** $`A \in \mathbb{R}^{3 \times 3}`$ can be **orthogonally diagonalized**, meaning:

$$
A = Q D Q^T
$$

Where:

* $`Q`$ is an **orthogonal matrix** ($`Q^T = Q^{-1}`$), whose columns are **orthonormal eigenvectors** of $`A`$


* $`D`$ is a **diagonal matrix** whose diagonal entries are the **real eigenvalues** of $`A`$

---

## **2. Properties of Real Symmetric Matrices**

A matrix $`A = A^T`$ satisfies:

* All eigenvalues are **real**


* There exists a set of **orthonormal eigenvectors**


* The matrix is always **diagonalizable via an orthogonal matrix**

---

## **3. General Form of a 3×3 Symmetric Matrix**

$$
A = \begin{bmatrix}
a & d & e \\
d & b & f \\
e & f & c
\end{bmatrix}
$$

Where $`a, b, c, d, e, f \in \mathbb{R}`$ and $`A = A^T`$.

---

## **4. Steps to Orthogonally Diagonalize a 3×3 Symmetric Matrix**

### **Step 1: Find Eigenvalues**

Solve the **characteristic polynomial**:

$$
\det(A - \lambda I) = 0
$$

This cubic equation gives **real eigenvalues** $`\lambda_1, \lambda_2, \lambda_3`$ (possibly repeated).

---

### **Step 2: Find Orthonormal Eigenvectors**

For each eigenvalue $`\lambda_i`$:

* Solve:

$$
(A - \lambda_i I)\mathbf{v}_i = 0
$$

* Find **linearly independent** eigenvectors for repeated eigenvalues.


* Use the **Gram-Schmidt process** if necessary to orthonormalize the vectors.


* Normalize:

$$
\mathbf{q}_i = \frac{\mathbf{v}_i}{\|\mathbf{v}_i\|}
$$

---

### **Step 3: Form $`Q`$ and $`D`$**

Let:

* $`Q = [\mathbf{q}_1 \ \mathbf{q}_2 \ \mathbf{q}_3]`$


* 
$$ = \begin{bmatrix}\ \lambda\_1 & 0 & 0 \\ 0 & \lambda\_2 & 0 \\ 0 & 0 & \lambda\_3 \end{bmatrix}\ $$



Then:

$$
A = Q D Q^T
$$

---

## **5. Identifying Parts of an Orthogonal Diagonalization**

If **partial information** is given (e.g., one eigenvalue/vector or part of $`Q`$ or $`D`$), use:

* $`A Q = Q D`$


* Orthogonality: all eigenvectors must be **mutually orthogonal**


* Use the structure of $Q$ (columns are orthonormal eigenvectors) to deduce missing entries

---

## **6. Orthogonally Diagonalizing a 3×3 Matrix With Distinct Eigenvalues**

### Example:

Let:

$$
A = \begin{bmatrix}
2 & 0 & 0 \\
0 & 3 & 4 \\
0 & 4 & 9
\end{bmatrix}
$$

* Step 1: Find eigenvalues $`\lambda_1, \lambda_2, \lambda_3`$


* Step 2: Solve $`(A - \lambda_i I)\mathbf{v}_i = 0`$ for each $`\lambda_i`$


* Step 3: Normalize the eigenvectors


* Step 4: Form $`Q`$ from the orthonormal eigenvectors


* Step 5: Compute $`D = Q^T A Q`$

---


## **7. Orthogonally Diagonalizing a 3×3 Matrix With Repeated Eigenvalues**

If eigenvalues repeat (e.g., $`\lambda = 5`$ with multiplicity 2):

* Ensure the **algebraic multiplicity** equals the **geometric multiplicity**


* Find **two linearly independent eigenvectors** for $`\lambda`$


* Orthonormalize them


* Proceed as usual with $Q$ and $D$

---

## Summary Table

| **Component**                        | **Meaning**                       |
| ------------------------------------ | --------------------------------- |
| Symmetric matrix $`A`$                 | $`A^T = A`$                         |
| Eigenvalues of $`A`$                   | All real, possibly repeated       |
| Eigenvectors of distinct eigenvalues | Always orthogonal                 |
| Orthonormal eigenvectors             | Normalize using Euclidean norm    |
| Orthogonal diagonalization           | $`A = Q D Q^T`$                     |
| $`Q`$                                  | Orthogonal matrix: $`Q^T = Q^{-1}`$ |
| $`D`$                                  | Diagonal matrix of eigenvalues    |

---