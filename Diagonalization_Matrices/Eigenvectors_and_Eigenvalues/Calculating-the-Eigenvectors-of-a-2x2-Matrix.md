## **Calculating the Eigenvectors of a 2x2 Matrix**

---

## 1. Calculating the Components of an Eigenvector Corresponding to an Eigenvalue

Given a $`2 \times 2`$ matrix:

$$
A = \begin{pmatrix} a & b \\ c & d \end{pmatrix}
$$

And an eigenvalue $`\lambda`$, solve the equation:

$$
(A - \lambda I)\vec{v} = \vec{0}
$$

This gives a homogeneous system:

$$
\begin{pmatrix} a - \lambda & b \\ c & d - \lambda \end{pmatrix} \begin{pmatrix} x \\ y \end{pmatrix} = \begin{pmatrix} 0 \\ 0 \end{pmatrix}
$$

To find the components $`(x, y)`$ of the eigenvector $`\vec{v}`$, reduce the matrix to row echelon form 
and solve for $`x`$ and $`y`$ (usually up to scalar multiple).

---

## 2. Calculating an Eigenvector Corresponding to an Eigenvalue

### **Step-by-step Example:**

Let:

$$
A = \begin{pmatrix} 4 & 1 \\ 2 & 3 \end{pmatrix}
$$

### Step 1: Find eigenvalues by solving:

$$
\det(A - \lambda I) = 0
$$

$$
\begin{vmatrix} 4 - \lambda & 1 \\ 2 & 3 - \lambda \end{vmatrix} = (4 - \lambda)(3 - \lambda) - 2 = \lambda^2 - 7\lambda + 10 = 0
$$

Eigenvalues: $`\lambda = 5, 2`$

### Step 2: Pick $`\lambda = 5`$

Solve $`(A - 5I)\vec{v} = \vec{0}`$:

$$
\begin{pmatrix} -1 & 1 \\ 2 & -2 \end{pmatrix} \begin{pmatrix} x \\ y \end{pmatrix} = \vec{0}
$$

This reduces to $`x = y`$, so an eigenvector is:

$$
\vec{v}_1 = \begin{pmatrix} 1 \\ 1 \end{pmatrix}
$$

---

## 3. Finding Two Linearly Independent Eigenvectors of a 2x2 Matrix

If a $`2 \times 2`$ matrix has **two distinct eigenvalues**, then the corresponding eigenvectors will be **linearly independent**.

From the example above:

* Eigenvalue $`\lambda = 5`$ ⇒ $`\vec{v}\_1 = \begin{pmatrix} 1 \ 1 \end{pmatrix}`$
* Eigenvalue $`\lambda = 2`$ ⇒ Solve:

$$
\begin{pmatrix} 2 & 1 \\ 2 & 1 \end{pmatrix} \vec{v} = \vec{0} \Rightarrow x = -0.5y
$$

Eigenvector:

$$
\vec{v}_2 = \begin{pmatrix} -1 \\ 2 \end{pmatrix}
$$

Thus, $`\vec{v}\_1`$ and $`\vec{v}\_2`$ are linearly independent.

---

## Summary

| Task                | Procedure                                                        |
| ------------------- | ---------------------------------------------------------------- |
| Find eigenvalues    | Solve $`\det(A - \lambda I) = 0`$                                |
| Find eigenvectors   | Solve $`(A - \lambda I)\vec{v} = \vec{0}`$ for each $`\lambda`$   |
| Linear independence | If eigenvalues are distinct, eigenvectors are linearly independent |

---
