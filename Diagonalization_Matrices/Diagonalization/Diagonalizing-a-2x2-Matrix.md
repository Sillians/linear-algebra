## **Diagonalizing a 2×2 Matrix**

---

## **I. What Does It Mean to Diagonalize a Matrix?**

A 2×2 matrix $A$ is **diagonalizable** if there exists an invertible matrix $P$ and a diagonal matrix $D$ such that:

$$
A = P D P^{-1}
$$

* The columns of $P$ are **eigenvectors** of $A$.
* The diagonal entries of $D$ are the corresponding **eigenvalues**.

---

## **II. Step-by-Step: Diagonalizing a 2×2 Matrix**

Given a matrix:

$$
A = \begin{bmatrix}
a & b \\
c & d
\end{bmatrix}
$$

### **Step 1: Find the Eigenvalues**

Solve the **characteristic equation**:

$$
\det(A - \lambda I) = 0
$$

$$
\Rightarrow \det\begin{bmatrix}
a - \lambda & b \\
c & d - \lambda
\end{bmatrix} = (a - \lambda)(d - \lambda) - bc = 0
$$

This gives a quadratic equation in $`\lambda`$. Solve it to get eigenvalues $`\lambda_1`$, $`\lambda_2`$.

---

### **Step 2: Find the Eigenvectors**

For each eigenvalue $`\lambda`$, solve:

$$
(A - \lambda I)\vec{v} = 0
$$

This gives an eigenvector $`\vec{v}`$ for each $`\lambda`$.

---

### **Step 3: Form $`P`$ and $`D`$**

* Let $`P = [\vec{v}_1 \,\, \vec{v}_2]`$


* Let $`D = \begin{bmatrix} \lambda_1 & 0 \\ 0 & \lambda_2 \end{bmatrix}`$

---

## **III. Diagonalizing a 2x2 Matrix Given Its Eigenvalues**

If eigenvalues $`\lambda_1`$ and $`\lambda_2`$ are **distinct**, then:

* The matrix is **guaranteed to be diagonalizable**.
* You just need to compute the eigenvectors as described above.

**Example:**

$$
A = \begin{bmatrix}
2 & 1 \\
0 & 3
\end{bmatrix}
$$

Characteristic equation:

$$
(2 - \lambda)(3 - \lambda) = 0 \Rightarrow \lambda = 2, 3
$$

Eigenvectors:

* For $`\lambda = 2`$: Solve $`(A - 2I)\vec{v} = 0`$
* For $`\lambda = 3`$: Solve $`(A - 3I)\vec{v} = 0`$

Then form $P$ and $D$ as in Step 3.

---

## **IV. Identifying Whether a 2×2 Matrix Is Diagonalizable**

A 2×2 matrix is diagonalizable **if and only if** it has **two linearly independent eigenvectors**.

Use these checks:

* **Distinct eigenvalues?** ⇒ Always diagonalizable.
* **Repeated eigenvalue?**

  * If **algebraic multiplicity = geometric multiplicity**, it's diagonalizable.
  * If not, it's **not diagonalizable**.

**Example (not diagonalizable):**

$$
A = \begin{bmatrix}
4 & 1 \\
0 & 4
\end{bmatrix}
$$

Only eigenvalue: $`\lambda = 4`$

$$
(A - 4I) = \begin{bmatrix}
0 & 1 \\
0 & 0
\end{bmatrix}
\Rightarrow \text{1 eigenvector only} \Rightarrow \text{Not diagonalizable}
$$

---

## **V. Diagonalizing a 2x2 Matrix Given Part of the Diagonalization**

If you're given $P$ or $D$ partially, you can recover the rest using:

$$
A = P D P^{-1}
\Rightarrow A P = P D
$$

So, if you know $A$ and $P$, compute $`D = P^{-1} A P`$

Or, if you know $D$ and $P$, compute $`A = P D P^{-1}`$

**Example:**

Given:

* $`P = \begin{bmatrix} 1 & 1 \\ 0 & 1 \end{bmatrix}`$
* $`D = \begin{bmatrix} 2 & 0 \\ 0 & 3 \end{bmatrix}`$

Then:

$$
A = P D P^{-1}
\Rightarrow A = \begin{bmatrix} 1 & 1 \\ 0 & 1 \end{bmatrix}
\begin{bmatrix} 2 & 0 \\ 0 & 3 \end{bmatrix}
\begin{bmatrix} 1 & -1 \\ 0 & 1 \end{bmatrix}
= \begin{bmatrix} 2 & 1 \\ 0 & 3 \end{bmatrix}
$$

---

## **VI. Summary Table**

| Step | Action                                                 |
| ---- | ------------------------------------------------------ |
| 1    | Solve $`\det(A - \lambda I) = 0`$ for eigenvalues        |
| 2    | For each $`\lambda`$, solve $`(A - \lambda I)\vec{v} = 0`$ |
| 3    | Construct matrix $P$ from eigenvectors                 |
| 4    | Construct $D$ from eigenvalues                         |
| 5    | Check: $`A = P D P^{-1}`$                                |

---

## **VII. Quick Tip**

A 2×2 matrix with:

* **Distinct eigenvalues** ⇒ Always diagonalizable
* **Repeated eigenvalues** ⇒ Diagonalizable **only if** 2 linearly independent eigenvectors exist


