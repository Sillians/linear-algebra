# **Diagonalization of 2×2 Symmetric Matrices**

---

## **1. Overview**

A **real symmetric matrix** $`A \in \mathbb{R}^{2 \times 2}`$ can always be **orthogonally diagonalized**, meaning:

$$
A = Q D Q^T
$$

Where:

* $`Q`$ is an **orthogonal matrix** whose columns are eigenvectors of $`A`$


* $`D`$ is a **diagonal matrix** of eigenvalues


* $`Q^T = Q^{-1}`$

---

## **2. Properties of Symmetric Matrices**

For any **symmetric matrix** $`A = A^T`$:

* All eigenvalues are **real**
* Eigenvectors corresponding to **distinct eigenvalues** are **orthogonal**
* There exists an **orthogonal matrix** $`Q`$ such that:

$$
Q^T A Q = D \quad \text{(Diagonal matrix)}
$$

---

## **3. General Form of a 2×2 Symmetric Matrix**

A 2×2 symmetric matrix has the form:

$$
A = \begin{bmatrix}
a & b \\
b & d
\end{bmatrix}
$$

Where $`a, b, d \in \mathbb{R}`$ and $`b = b^T`$.

---

## **4. Steps to Orthogonally Diagonalize a 2×2 Symmetric Matrix**

### Step 1: Find the eigenvalues

Solve the **characteristic polynomial**:

$$
\det(A - \lambda I) = 0
$$

This gives the **eigenvalues** $`\lambda_1, \lambda_2`$.

### Step 2: Find orthonormal eigenvectors

* Solve $`(A - \lambda_i I)\mathbf{v}_i = 0`$ for each eigenvalue


* Normalize the eigenvectors:

$$
\mathbf{q}_i = \frac{\mathbf{v}_i}{\|\mathbf{v}_i\|}
$$


### Step 3: Form matrices $Q$ and $D$

* $`Q = [\mathbf{q}_1 \,\, \mathbf{q}_2]`$ (orthonormal eigenvectors)


* $`D = \begin{bmatrix} \lambda_1 & 0 \\ 0 & \lambda_2 \end{bmatrix}`$

Then:

$$
A = Q D Q^T
$$

---

## **5. Identifying Parts of an Orthogonal Diagonalization**

Given partial info, such as:

* One eigenvector


* One eigenvalue


* A diagonalized matrix


You can deduce the missing parts using:

* Orthogonality of eigenvectors


* Matrix multiplication:

$$
A Q = Q D
$$

---

## **6. Example: Orthogonally Diagonalizing a 2×2 Symmetric Matrix**

Let:

$$
A = \begin{bmatrix}
4 & 2 \\
2 & 3
\end{bmatrix}
$$

### Step 1: Find eigenvalues

Solve:

$$
\det(A - \lambda I) = 
\begin{vmatrix}
4 - \lambda & 2 \\
2 & 3 - \lambda
\end{vmatrix}
= (4 - \lambda)(3 - \lambda) - 4 = \lambda^2 - 7\lambda + 8 = 0
$$

Eigenvalues:

$$
\lambda_1 = 4 + \sqrt{2}, \quad \lambda_2 = 4 - \sqrt{2}
$$

### Step 2: Find eigenvectors

For each eigenvalue, solve $`(A - \lambda I)\mathbf{v} = 0`$, then normalize.

Let’s say:

* $`\mathbf{v}_1 = \begin{bmatrix} 1 \\ \alpha \end{bmatrix}`$ for $`\lambda_1`$


* $`\mathbf{v}_2 = \begin{bmatrix} 1 \\ \beta \end{bmatrix}`$ for $`\lambda_2`$

Normalize each to get $`\mathbf{q}_1, \mathbf{q}_2`$.

### Step 3: Form $`Q`$ and $`D`$

Let:

$$
Q = [\mathbf{q}_1 \,\, \mathbf{q}_2], \quad D = \begin{bmatrix} \lambda_1 & 0 \\ 0 & \lambda_2 \end{bmatrix}
$$

Then:

$$
A = Q D Q^T
$$

---

## **7. Orthogonally Diagonalizing a 2×2 Symmetric Matrix Given Part of the Diagonalization**

### Scenario:

Given:

* One eigenvalue $`\lambda_1`$


* A vector $`\mathbf{q}_1`$

Then:

* Use $`A\mathbf{q}_1 = \lambda_1 \mathbf{q}_1`$ to verify or complete $`\mathbf{q}_1`$


* Find $`\mathbf{q}_2`$ orthogonal to $`\mathbf{q}_1`$


* Normalize $`\mathbf{q}_2`$


* Compute second eigenvalue $`\lambda_2`$ from:

$$
A\mathbf{q}_2 = \lambda_2 \mathbf{q}_2
$$

---

## Summary Table

| **Component**                         | **Meaning**                                     |
|---------------------------------------| ----------------------------------------------- |
| Symmetric matrix $`A`$                | $`A^T = A`$                                       |
| Orthogonal matrix $`Q`$               | $`Q^T Q = I`$, columns = orthonormal eigenvectors |
| Diagonal matrix $`D`$                 | Contains real eigenvalues of $`A`$                |
| Diagonalization                       | $`A = Q D Q^T`$                                   |
| Eigenvectors of distinct eigenvalues  | Orthogonal                                      |
| Diagonalization preserves             | Lengths, angles (when $`Q`$ orthogonal)           |

---
