# **Calculating the Eigenvectors of a 3×3 Matrix**

## **1. Overview**

Given a $`3 \times 3`$ matrix $`A`$, eigenvectors are the nonzero vectors $`\mathbf{v}`$ such that:

$$
A\mathbf{v} = \lambda\mathbf{v}
$$

To find eigenvectors:

1. Solve the **characteristic equation** $`\det(A - \lambda I) = 0`$ to get eigenvalues $`\lambda`$.
2. For each eigenvalue $`\lambda`$, solve:

$$
(A - \lambda I)\mathbf{v} = \mathbf{0}
$$

This is a **homogeneous linear system**, and its solution set (excluding the zero vector) gives the eigenspace for $`\lambda`$.

---

## **2. Finding Linearly Independent Eigenvectors of a 3×3 Matrix**

* Each distinct eigenvalue guarantees a **linearly independent eigenvector**.
* If eigenvalues are repeated, the **algebraic multiplicity** (number of times $`\lambda`$ appears in the characteristic polynomial) must be compared to the **geometric multiplicity** (dimension of eigenspace).

> If geometric multiplicity = algebraic multiplicity → matrix is diagonalizable.

### **Example**

Let:

$$
A = \begin{bmatrix}
4 & 1 & 0 \\
0 & 2 & 0 \\
0 & 0 & 2
\end{bmatrix}
$$

Eigenvalues: $`\lambda = 4`$ and $`\lambda = 2`$ (with multiplicity 2).

* For $`\lambda = 4`$: Solve $`(A - 4I)\mathbf{v} = 0`$
* For $`\lambda = 2`$: Solve $`(A - 2I)\mathbf{v} = 0`$

Check that the eigenspace for $`\lambda = 2`$ has dimension 2 ⇒ matrix is diagonalizable.

---

## **3. Finding a Basis of a One-Dimensional Eigenspace**

Let $A$ have an eigenvalue $`\lambda`$ with **algebraic multiplicity 1**.

* Solve $`(A - \lambda I)\mathbf{v} = 0`$
* Use row reduction to find the nullspace
* Basis will contain **1 non-zero vector**

### Example

If:

$$
A = \begin{bmatrix}
3 & 0 & 0 \\
0 & 2 & 1 \\
0 & 0 & 2
\end{bmatrix}, \quad \lambda = 3
$$

Then:

$$
A - 3I = \begin{bmatrix}
0 & 0 & 0 \\
0 & -1 & 1 \\
0 & 0 & -1
\end{bmatrix}
$$

Solving gives a one-dimensional eigenspace ⇒ basis with one vector.

---

## **4. Finding a Basis of a Two-Dimensional Eigenspace**

Let $`\lambda`$ have **geometric multiplicity 2**.

* Solve $`(A - \lambda I)\mathbf{v} = 0`$
* Reduce the system to get a solution space with **2 free variables**
* Basis will contain **2 linearly independent vectors**

---

## **5. Calculating the Dimension of an Eigenspace**

Given an eigenvalue $`\lambda`$, the **dimension of the eigenspace** is:

$$
\dim(\ker(A - \lambda I))
$$

It equals the number of linearly independent solutions of $`(A - \lambda I)\mathbf{v} = 0`$.

> Use Gaussian elimination to determine the number of free variables = dimension of the eigenspace.

---


Here’s a **fully worked example** of **calculating the eigenvectors of a 3×3 matrix**, including:

* Finding eigenvalues
* Finding linearly independent eigenvectors
* Determining eigenspaces and their dimensions
* Verifying diagonalizability

---

## **🔢 Example Matrix**

Let:

$$
A = \begin{bmatrix}
4 & 1 & -1 \\
1 & 4 & -1 \\
-1 & -1 & 4
\end{bmatrix}
$$

---

### **Step 1: Find the Eigenvalues**

Solve the **characteristic equation**:

$$
\det(A - \lambda I) = 0
$$

So,

$$
\det\begin{bmatrix}
4 - \lambda & 1 & -1 \\
1 & 4 - \lambda & -1 \\
-1 & -1 & 4 - \lambda
\end{bmatrix} = 0
$$

Expanding the determinant (using cofactor expansion or a symbolic tool):

$$
\Rightarrow (4 - \lambda)^3 - 3(4 - \lambda) - 2 = 0
$$

After simplification, eigenvalues are:

$$
\lambda_1 = 6, \quad \lambda_2 = 3, \quad \lambda_3 = 3
$$

---

### **Step 2: Eigenvectors for $`\lambda = 6`$**

Solve:

$$
(A - 6I)\mathbf{v} = 0
$$

That is,

$$
\begin{bmatrix}
-2 & 1 & -1 \\
1 & -2 & -1 \\
-1 & -1 & -2
\end{bmatrix} \begin{bmatrix} x \\ y \\ z \end{bmatrix} = \begin{bmatrix} 0 \\ 0 \\ 0 \end{bmatrix}
$$

Row reducing:

$$
\Rightarrow \text{Null space basis: } \begin{bmatrix} 1 \\ 1 \\ -1 \end{bmatrix}
$$

So, the **eigenspace** for $`\lambda = 6`$ is 1-dimensional.

---

### **Step 3: Eigenvectors for \$\lambda = 3\$**

Solve:

$$
(A - 3I)\mathbf{v} = 0
$$

That is,

$$\begin{bmatrix} 1 & 1 & -1 \\ 1 & 1 & -1 \\ -1 & -1 & 1 \end{bmatrix} \begin{bmatrix} x \\ y \\ z \end{bmatrix} = \begin{bmatrix} 0 \\ 0 \\ 0 \end{bmatrix}$$

Reducing gives:

$$
x + y - z = 0 \quad \Rightarrow \quad x = z - y
$$

Let $`y = s`$, $`z = t`$, then:

$$
\mathbf{v} = \begin{bmatrix} t - s \\ s \\ t \end{bmatrix}
= s\begin{bmatrix} -1 \\ 1 \\ 0 \end{bmatrix} + t\begin{bmatrix} 1 \\ 0 \\ 1 \end{bmatrix}
$$

So, **basis**:

* $`\begin{bmatrix} -1 \ 1 \ 0 \end{bmatrix}`$
* $`\begin{bmatrix} 1 \ 0 \ 1 \end{bmatrix}`$

Eigenspace for $`\lambda = 3`$ is **2-dimensional**.

---

### **Step 4: Summary**

| Eigenvalue     | Basis of Eigenspace                                                                                  | Dimension |
| -------------- |------------------------------------------------------------------------------------------------------| --------- |
| $`\lambda = 6`$ | $`  \begin{bmatrix} 1 \ 1 \ -1 \end{bmatrix} `$                                          | 1         |
| $`\lambda = 3`$ | $`\begin{bmatrix} -1 \ 1 \ 0 \end{bmatrix}, \begin{bmatrix} 1 \ 0 \ 1 \end{bmatrix} `$ | 2         |

---

### ✅ **Diagonalizability**

Since the sum of eigenspace dimensions = 3 (equal to the size of the matrix), $A$ is **diagonalizable**.



## **Conclusion**

| Topic        | Key Tool                              |
| ------------ | ------------------------------------- |
| Eigenvalues  | Solve $`\det(A - \lambda I) = 0`$     |
| Eigenvectors | Solve $`(A - \lambda I)\mathbf{v} = 0`$ |
| Basis        | Nullspace of $`(A - \lambda I)`$       |
| Dimension    | Rank-Nullity Theorem                  |
| Independence | Check vector spans                    |

