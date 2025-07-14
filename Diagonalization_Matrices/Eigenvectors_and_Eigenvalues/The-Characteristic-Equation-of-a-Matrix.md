## **The Characteristic Equation of a Matrix**

---

## **I. What Is the Characteristic Equation?**

The **characteristic equation** of a square matrix $`A \in \mathbb{R}^{n \times n}`$ is the **determinant equation** used to find its **eigenvalues**.

$$
\text{Characteristic equation: } \det(A - \lambda I) = 0
$$

* $`\lambda \in \mathbb{C}`$ are the eigenvalues of $A$
* $I$ is the identity matrix
* $`\det(A - \lambda I)`$ is a **polynomial** of degree $n$

Solving this equation gives the **eigenvalues** of the matrix.

---

## **II. Key Concepts**

| Term                      | Meaning                                                                |
| ------------------------- | ---------------------------------------------------------------------- |
| Characteristic Polynomial | $`p(\lambda) = \det(A - \lambda I)`$                                     |
| Eigenvalue                | Scalar $`\lambda`$ for which $`A\vec{v} = \lambda\vec{v}`$                 |
| Algebraic Multiplicity    | The multiplicity of $`\lambda`$ as a root of the characteristic equation |

---

## **III. Finding the Characteristic Equation of an $`n \times n`$ Matrix**

### **General Steps:**

1. Construct $`A - \lambda I`$
2. Compute the determinant: $`\det(A - \lambda I)`$
3. Set it equal to zero: $`\det(A - \lambda I) = 0`$
4. Solve the resulting polynomial equation for $`\lambda`$

---

## **IV. Finding Eigenvalues of a General 3×3 Matrix**

Let:

$$
A = \begin{bmatrix}
a & b & c \\
d & e & f \\
g & h & i
\end{bmatrix}
$$

Compute $`\det(A - \lambda I)`$:

$$
A - \lambda I = \begin{bmatrix}
a - \lambda & b & c \\
d & e - \lambda & f \\
g & h & i - \lambda
\end{bmatrix}
$$

Then compute:

$$
\det(A - \lambda I) = -\lambda^3 + \text{(trace-related and cofactor terms)}
$$

This gives a **cubic polynomial**, which may be factorable using:

* Rational root theorem
* Factorization by grouping
* Substitution (especially for symmetric or triangular matrices)

Solve this cubic for $`\lambda_1, \lambda_2, \lambda_3`$

---

## **V. Calculating the Eigenvalues of a 3×3 Matrix Containing a Block of Zeros**

A 3×3 matrix with a block of zeros can often be **simplified** using cofactor expansion or block matrix properties.

**Example:**

$$
A = \begin{bmatrix}
2 & 0 & 0 \\
1 & 3 & 4 \\
0 & 0 & 5
\end{bmatrix}
$$

Then:

$$
\det(A - \lambda I) = \det\begin{bmatrix}
2 - \lambda & 0 & 0 \\
1 & 3 - \lambda & 4 \\
0 & 0 & 5 - \lambda
\end{bmatrix}
$$

Use **cofactor expansion**:

$$
= (2 - \lambda)\cdot \det\begin{bmatrix}
3 - \lambda & 4 \\
0 & 5 - \lambda
\end{bmatrix}
= (2 - \lambda)(3 - \lambda)(5 - \lambda)
$$

**Eigenvalues:** $`\lambda = 2, 3, 5`$

Block structures often **diagonalize easily** or allow partial triangularization.

---

## **VI. Calculating the Eigenvalues of a 4×4 Matrix Containing a Block of Zeros**

For a 4×4 matrix with a zero block (e.g., upper triangular, block-diagonal), factorization becomes easier.

**Example (Block Diagonal):**

$$
A = \begin{bmatrix}
1 & 0 & 0 & 0 \\
0 & 2 & 0 & 0 \\
0 & 0 & 3 & 1 \\
0 & 0 & 0 & 3
\end{bmatrix}
$$

$$
\det(A - \lambda I) = (1 - \lambda)(2 - \lambda)\cdot \det\begin{bmatrix}
3 - \lambda & 1 \\
0 & 3 - \lambda
\end{bmatrix}
$$

$$
= (1 - \lambda)(2 - \lambda)(3 - \lambda)^2
$$

**Eigenvalues:** $`\lambda = 1, 2, 3`$ (multiplicity 2 for 3)

**Key Insight:** Upper/lower triangular and block matrices have **eigenvalues = diagonal entries**.

---

## **VII. Summary Table**

| Matrix Type             | Characteristic Equation                         | Notes                       |
| ----------------------- | ----------------------------------------------- | --------------------------- |
| 2×2 Matrix              | $`\lambda^2 - \text{tr}(A)\lambda + \det(A) = 0`$ | Quadratic                   |
| 3×3 General Matrix      | $`\lambda^3 + a\lambda^2 + b\lambda + c = 0`$     | Cubic; solve via factoring  |
| 3×3 with Zero Block     | Factor using cofactor expansion                 | Often separable             |
| 4×4 with Block Diagonal | Characteristic polynomial is product of blocks  | Block decomposition helpful |

---

## **VIII. Final Notes**

* For larger matrices, symbolic computation or numerical solvers (like characteristic polynomial factorization, QR algorithm, or eigenvalue routines in NumPy/SciPy) are typically used.
* Identifying structure (triangular, block diagonal, sparse) can simplify eigenvalue computation dramatically.
