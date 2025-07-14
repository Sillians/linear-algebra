# **Calculating the Eigenvectors of a 3×3 Matrix With Distinct Eigenvalues**

---

### Overview

When a 3×3 matrix has **three distinct eigenvalues**, it is **diagonalizable**, and each eigenvalue corresponds to **exactly one linearly independent eigenvector**. 
This allows the construction of a basis of eigenvectors that spans $`\mathbb{R}^3`$.

---

###  Step-by-Step Process

Given a matrix $`A \in \mathbb{R}^{3 \times 3}`$:

1. **Compute the characteristic polynomial**:

$$
\det(A - \lambda I) = 0
$$

2. **Find the eigenvalues**: Solve the cubic equation to get distinct eigenvalues $`\lambda_1, \lambda_2, \lambda_3`$.

3. **Find eigenvectors** for each $`\lambda_i`$ by solving:

$$
(A - \lambda_i I)\vec{x} = \vec{0}
$$

---

###  Calculating the Components of an Eigenvector Corresponding to a Given Eigenvalue

Let one eigenvalue be $`\lambda`$. To find the components of the corresponding eigenvector $`\vec{x}`$:

* Solve the homogeneous system:

$$
(A - \lambda I)\vec{x} = \vec{0}
$$

* The solution space gives the **null space**, and any nonzero vector in it (up to a scalar multiple) is an eigenvector.

---

### Calculating an Eigenvector Corresponding to a Given Eigenvalue

For a given $`\lambda`$:

1. Compute $`(A - \lambda I)`$.
2. Row reduce to RREF.
3. Solve:

$$
\vec{x} \in \text{Null}(A - \lambda I)
$$

---

### Finding the Eigenvectors of a 3×3 Matrix

Repeat the process for each eigenvalue:

* Compute $`(A - \lambda_i I)`$.
* Solve $`(A - \lambda_i I)\vec{x} = \vec{0}`$.
* Each nonzero solution $`\vec{v}_i`$ is an eigenvector.

This yields a set of eigenvectors:

$$
\{ \vec{v}_1, \vec{v}_2, \vec{v}_3 \}
$$

that form a basis for $`\mathbb{R}^3`$ if the eigenvalues are distinct.

---

###  Summary

* A 3×3 matrix with **distinct eigenvalues** always has **3 linearly independent eigenvectors**.
* Each eigenvector solves $`(A - \lambda I)\vec{x} = \vec{0}`$.
* These vectors form an **eigenbasis** and can be used to **diagonalize** the matrix.

---
