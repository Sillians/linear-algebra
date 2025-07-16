#  Constrained Optimization of Quadratic Forms

---

##  Overview

A **quadratic form** in $`\mathbb{R}^n`$ is an expression of the form:

$$
Q(\mathbf{x}) = \mathbf{x}^T A \mathbf{x}
$$

Where:

* $`\mathbf{x} \in \mathbb{R}^n`$ is a column vector


* $`A`$ is a **symmetric** $`n \times n`$ matrix

The optimization problem:

> **Maximize or minimize** $`Q(\mathbf{x})`$ **subject to** $`|\mathbf{x}| = 1`$

is a **constrained optimization** problem on the **unit sphere** $`S^{n-1}`$.

---

##  Method: Lagrange Multipliers

To solve:

$$
\text{Optimize } Q(\mathbf{x}) = \mathbf{x}^T A \mathbf{x} \quad \text{subject to } \|\mathbf{x}\|^2 = 1
$$

Define the **Lagrangian**:

$$
\mathcal{L}(\mathbf{x}, \lambda) = \mathbf{x}^T A \mathbf{x} - \lambda(\mathbf{x}^T \mathbf{x} - 1)
$$

Take the gradient:

$$
\nabla_{\mathbf{x}} \mathcal{L} = 2A\mathbf{x} - 2\lambda \mathbf{x} = 0 \Rightarrow A\mathbf{x} = \lambda \mathbf{x}
$$

So, **stationary points** of the quadratic form on the unit sphere occur at the **eigenvectors** of $A$,
and the **extreme values** are the corresponding **eigenvalues**.

---

##  Finding the Maximum Value (Canonical Form)

For a diagonal quadratic form:

$$
Q(\mathbf{x}) = \lambda_1 x_1^2 + \lambda_2 x_2^2 + \cdots + \lambda_n x_n^2, \quad \text{with } \|\mathbf{x}\| = 1
$$

To **maximize** $Q$, choose the coordinate with the **largest $`\lambda\_i`$**:

* Let $`x\_i = 1`$ and all other components be zero
* Then $`Q(\mathbf{x}) = \lambda\_i`$

**Result**: The **maximum value** is $`\max(\lambda\_1, \dots, \lambda\_n)`$

---

##  Finding the Minimum Value (Canonical Form)

Similarly, to **minimize** $Q$:

* Choose $`x\_i = 1`$ for the index $`i`$ corresponding to the **smallest $`\lambda\_i`$**
* All other $`x\_j = 0`$

**Result**: The **minimum value** is $`\min(\lambda\_1, \dots, \lambda\_n)`$

---

##  General Case: Max & Min Values on the Unit Sphere

Let $A$ be a symmetric matrix with real eigenvalues:

$$
\lambda_1 \leq \lambda_2 \leq \dots \leq \lambda_n
$$

Then:

* **Minimum** of $`Q(\mathbf{x}) = \mathbf{x}^T A \mathbf{x}`$ on $`|\mathbf{x}| = 1`$ is $`\lambda\_1`$


* **Maximum** is $`\lambda\_n`$

These occur at the **unit eigenvectors** of $A$ corresponding to $`\lambda\_1`$ and $`\lambda\_n`$ respectively.

---

##  Example

Let:

$$
Q(\mathbf{x}) = x_1^2 + 2x_2^2 + 3x_3^2 \quad \text{subject to } x_1^2 + x_2^2 + x_3^2 = 1
$$

This corresponds to the matrix:

$$
A = \begin{bmatrix}
1 & 0 & 0 \\
0 & 2 & 0 \\
0 & 0 & 3
\end{bmatrix}
$$

Eigenvalues: $`\lambda\_1 = 1`$, $`\lambda\_2 = 2`$, $`\lambda\_3 = 3`$

* **Minimum**: 1, at $`\mathbf{x} = \begin{bmatrix} 1 \ 0 \ 0 \end{bmatrix}`$


* **Maximum**: 3, at $`\mathbf{x} = \begin{bmatrix} 0 \ 0 \ 1 \end{bmatrix}`$

---

## ✅ Summary Table

| **Goal**                                           | **Method**              | **Result**                                 |
|----------------------------------------------------| ----------------------- | ------------------------------------------ |
| Maximize $`Q(\mathbf{x})`$ on $`\|\mathbf{x}\|=1`$ | Lagrange multipliers     | Largest eigenvalue of $A$                 |
| Minimize $`Q(\mathbf{x})`$ on $`\|\mathbf{x}\|=1`$ | Lagrange multipliers    | Smallest eigenvalue of $A$                |
| Canonical Form Optimization                        | Direct substitution     | Max/min = largest/smallest diagonal        |
| General Case                                       | Eigenvalue decomposition | Solve $`A \mathbf{x} = \lambda \mathbf{x}`$ |

---

##  Final Insight

> The extrema of a symmetric quadratic form on the unit sphere are the **extreme eigenvalues** of its associated matrix, 
> and they occur at the corresponding **unit eigenvectors**.

---