# **The Least-Squares Solution of a Linear System (With Collinearity)**

When a system of linear equations is **overdetermined** or when the matrix of coefficients has **linearly dependent (collinear) columns**, 
the system may not have an exact solution. In such cases, we use the **least-squares approach** to find an approximate solution.

---

## What Is Collinearity?

In the context of linear systems, **collinearity** means that some columns of the matrix $A$ are linearly dependent 
(i.e., one is a scalar multiple or linear combination of the others).

* This causes $`A^T A`$ to be **singular** (not invertible)
* The normal equation method cannot proceed unless adjusted (e.g., using a **pseudo-inverse**)

---

##  The Least-Squares Problem

Given a matrix equation:

$$
A \mathbf{x} = \mathbf{b}
$$

where $`A \in \mathbb{R}^{m \times n}`$ (with $`m > n`$ or collinear columns), the **least-squares solution** minimizes the Euclidean norm of the residual:

$$
\min_{\mathbf{x}} \| A \mathbf{x} - \mathbf{b} \|^2
$$

---

## Constructing the Normal Equation

To find the least-squares solution, we derive the **normal equations**:

$$
A^T A \mathbf{x} = A^T \mathbf{b}
$$

If $`A^T A`$ is **invertible**, the solution is:

$$
\mathbf{x} = (A^T A)^{-1} A^T \mathbf{b}
$$

If $`A^T A`$ is **singular** (due to collinearity), use the **Moore-Penrose pseudo-inverse**:

$$
\mathbf{x} = A^{+} \mathbf{b}
$$

Where $`A^{+}`$ is computed via:

* SVD (Singular Value Decomposition), or
* Ridge regularization if necessary

---

##  Example: Least-Squares With Collinearity

Let:

$$
A = \begin{bmatrix}
1 & 2 \\
2 & 4 \\
3 & 6 \\
\end{bmatrix}, \quad
\mathbf{b} = \begin{bmatrix}
1 \\
2 \\
3 \\
\end{bmatrix}
$$

Note: The second column is twice the first → **perfect collinearity**.

1. Compute $`A^T A`$:

$$
A^T A = \begin{bmatrix}
14 & 28 \\
28 & 56 \\
\end{bmatrix}
$$

Singular → cannot invert.

2. Use SVD or pseudo-inverse:

Let $`\mathbf{x}\_{\text{ls}} = A^{+} \mathbf{b}`$

3. The solution lies in the subspace spanned by the independent column(s). One possible least-squares solution is:

$$
\mathbf{x}_{\text{ls}} = \begin{bmatrix}
0.2 \\
0.4 \\
\end{bmatrix}
$$

All solutions have the form:

$$
\mathbf{x}_{\text{ls}} = \mathbf{x}_0 + \alpha \mathbf{n}
$$

Where $`\mathbf{n}`$ is in the null space of $`A`$ (the direction of collinearity).

---

## Summary Table

| Step              | Description                              |
| ----------------- | ---------------------------------------- |
| $`A^T A`$ singular | Use pseudo-inverse                       |
| Normal equation   | $`A^T A \mathbf{x} = A^T \mathbf{b}`$    |
| General solution  | $`\mathbf{x} = A^+ \mathbf{b}`$           |
| Residual vector   | $`\mathbf{r} = \mathbf{b} - A \mathbf{x}`$ |

---
