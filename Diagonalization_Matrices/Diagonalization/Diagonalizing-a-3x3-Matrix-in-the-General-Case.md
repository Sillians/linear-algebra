#  Diagonalizing a 3×3 Matrix

---

## 1. What Is Diagonalization?

A square matrix $A$ is **diagonalizable** if:

$$
A = P D P^{-1}
$$

Where:

* $P$ is a matrix whose **columns are the eigenvectors** of $A$


* $D$ is a **diagonal matrix** whose **entries are the eigenvalues** of $A$


Diagonalization simplifies computations like matrix powers, exponentials, and solving systems.

---

## 2. General Steps to Diagonalize a 3×3 Matrix

### Step 1: Compute the Characteristic Polynomial

Solve the equation:

$$
\det(A - \lambda I) = 0
$$

This yields the eigenvalues $`\lambda\_1, \lambda\_2, \lambda\_3`$.

---

### Step 2: Find Eigenvectors

For each eigenvalue $`\lambda\_i`$, solve:

$$
(A - \lambda_i I)\mathbf{v} = 0
$$

This gives the eigenvectors corresponding to each eigenvalue.

---

### Step 3: Check for Diagonalizability

A $`3 \times 3`$ matrix $A$ is **diagonalizable** if it has **three linearly independent eigenvectors**, i.e., the **sum of the dimensions of all eigenspaces is 3**.

---

### Step 4: Construct $P$ and $D$

* Matrix $P$ contains the eigenvectors as columns:


$$
P = \begin{bmatrix} \mathbf{v}_1 & \mathbf{v}_2 & \mathbf{v}_3 \end{bmatrix}
$$

* Diagonal matrix \$D\$ contains the corresponding eigenvalues:

$$
D = \begin{bmatrix}
\lambda_1 & 0 & 0 \\
0 & \lambda_2 & 0 \\
0 & 0 & \lambda_3
\end{bmatrix}
$$

Then:

$$
A = P D P^{-1}
$$

---

## 3. Full Example

Let:

$$
A = \begin{bmatrix}
4 & 1 & -1 \\
1 & 4 & -1 \\
-1 & -1 & 4
\end{bmatrix}
$$

### Characteristic Polynomial:

$$
\det(A - \lambda I) = (\lambda - 6)(\lambda - 3)^2
$$

### Eigenvalues:

* $`\lambda\_1 = 6`$


* $`\lambda\_2 = \lambda\_3 = 3`$

### Eigenvectors:

* For $`\lambda\_1 = 6`$:

$$
\mathbf{v}_1 = \begin{bmatrix} 1 \\ 1 \\ -1 \end{bmatrix}
$$

* For $`\lambda\_2 = \lambda\_3 = 3`$:

$$
\mathbf{v}_2 = \begin{bmatrix} -1 \\ 1 \\ 0 \end{bmatrix}, \quad
\mathbf{v}_3 = \begin{bmatrix} 1 \\ 0 \\ 1 \end{bmatrix}
$$

### Construct $P$ and $D$:

$$
P = \begin{bmatrix}
1 & -1 & 1 \\
1 & 1 & 0 \\
-1 & 0 & 1
\end{bmatrix}, \quad
D = \begin{bmatrix}
6 & 0 & 0 \\
0 & 3 & 0 \\
0 & 0 & 3
\end{bmatrix}
$$

So:

$$
A = P D P^{-1}
$$

---

## 4. Diagonalizing Given Part of the Diagonalization

Suppose you're given:

* 1 or 2 eigenvectors


* Partial $`P`$ and $`D`$



**Steps:**

1. Use the known eigenvalue(s) and vector(s)


2. Compute missing eigenvectors using $`(A - \lambda I)\mathbf{v} = 0`$


3. Build full $P$, ensuring invertibility


4. Match eigenvalues to eigenvectors in $D$

---

## 5. Finding the Diagonal Matrix $D$

Once eigenvalues are found:

$$
D = \text{diag}(\lambda_1, \lambda_2, \lambda_3)
$$

The order of eigenvalues in $D$ must correspond to the order of the eigenvectors in $P$.

---

##  Summary

| Step | Description                                                  |
| ---- |--------------------------------------------------------------|
| 1    | Find eigenvalues: $`\det(A - \lambda I) = 0`$                |
| 2    | Solve $`(A - \lambda I)\mathbf{v} = 0`$ for each $`\lambda`$ |
| 3    | Ensure eigenvectors are linearly independent                 |
| 4    | Construct $P$ and $D$                                        |
| 5    | Verify: $`A = P D P^{-1}`$                                   |

---
