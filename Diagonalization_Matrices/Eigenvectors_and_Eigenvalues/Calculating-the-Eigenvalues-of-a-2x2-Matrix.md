## **Calculating the Eigenvalues of a 2x2 Matrix**

---

## 1. Finding the Characteristic Equation of a Matrix

Let

$$
A = \begin{pmatrix} a & b \\ c & d \end{pmatrix}
$$

The characteristic equation is obtained by solving:

$$
\det(A - \lambda I) = 0
$$

So we compute:

$$
\begin{vmatrix} a - \lambda & b \\ c & d - \lambda \end{vmatrix} = 0
$$

Which expands to:

$$
(a - \lambda)(d - \lambda) - bc = 0
$$

The characteristic polynomial becomes:

$$
\lambda^2 - (a + d)\lambda + (ad - bc) = 0
$$

---

## 2. Computing the Eigenvalues of a Matrix With Two Distinct Eigenvalues

Solve the quadratic equation:

$$
\lambda^2 - \text{Tr}(A)\lambda + \det(A) = 0
$$

Where:

* $`\text{Tr}(A) = a + d`$ is the trace of $`A`$
* $`\det(A) = ad - bc`$ is the determinant of $`A`$

Compute the discriminant:

$$
\Delta = (\text{Tr}(A))^2 - 4\det(A)
$$

If $`\Delta > 0`$, the matrix has **two distinct real eigenvalues**.

**Example:**
Let

$$
A = \begin{pmatrix} 2 & 1 \\ 1 & 2 \end{pmatrix}
$$

Then,

$$
\lambda^2 - 4\lambda + 3 = 0 \quad \Rightarrow \quad \lambda = 1, 3
$$

---

## 3. Computing the Eigenvalues of a Matrix With At Most One Distinct Eigenvalue

If the discriminant $`\Delta = 0`$, the matrix has a **repeated eigenvalue**.

**Example:**

$$
A = \begin{pmatrix} 4 & 2 \\ 0 & 4 \end{pmatrix}
$$

Then,

$$
\lambda^2 - 8\lambda + 16 = 0 \quad \Rightarrow \quad (\lambda - 4)^2 = 0 \quad \Rightarrow \quad \lambda = 4
$$

---

## 4. Calculating the Eigenvalues of a Triangular or Diagonal Matrix

For a **triangular** or **diagonal** matrix, the eigenvalues are the diagonal entries.

**Example:**

$$
A = \begin{pmatrix} 5 & 3 \\ 0 & -2 \end{pmatrix}
$$

Eigenvalues:

$$
\lambda = 5, -2
$$

---
