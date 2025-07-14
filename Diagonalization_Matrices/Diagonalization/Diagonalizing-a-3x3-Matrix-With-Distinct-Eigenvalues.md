## **Diagonalizing a 3×3 Matrix With Distinct Eigenvalues**

---

### **1. What Is Diagonalization?**

A square matrix $`A \in \mathbb{R}^{n \times n}`$ is **diagonalizable** if there exists an invertible matrix $`P`$ 
and a diagonal matrix $`D`$ such that:

$$
A = PDP^{-1}
$$

Where:

* Columns of $`P`$ are the **eigenvectors** of $`A`$,
* $`D`$ contains the corresponding **eigenvalues** along its diagonal.

---

### **2. Diagonalizing a Matrix With Distinct Eigenvalues**

If a matrix $`A`$ has **three distinct eigenvalues**, then it is **guaranteed to be diagonalizable** over the real (or complex) numbers.

---

#### **Steps:**

1. **Find Eigenvalues**:
   Solve the **characteristic equation**:

$$
\det(A - \lambda I) = 0
$$

2. **Find Eigenvectors**:
For each eigenvalue $`\lambda\_i`$, solve:

$$
(A - \lambda_i I)\mathbf{v}_i = 0
$$

3. **Form Matrix $P$**:

* Columns = eigenvectors $`\mathbf{v}\_1, \mathbf{v}\_2, \mathbf{v}\_3`$

4. **Form Diagonal Matrix $D$**:

* Diagonal entries = corresponding eigenvalues $`\lambda\_1, \lambda\_2, \lambda\_3`$

5. **Verify**:

$$
A = P D P^{-1}
$$

---

### **3. Diagonalizing a Matrix Given Its Eigenvalues and Eigenvectors**

Let:

* Eigenvalues: $`\lambda\_1, \lambda\_2, \lambda\_3`$
* Corresponding eigenvectors: $`\mathbf{v}\_1, \mathbf{v}\_2, \mathbf{v}\_3`$

Then:

* $`P = [\mathbf{v}\_1\ \mathbf{v}\_2\ \mathbf{v}\_3]`$
* $`D = \text{diag}(\lambda\_1, \lambda\_2, \lambda\_3)`$
* $`A = P D P^{-1}`$

---

### **4. Identifying Diagonalizability Over $`\mathbb{R}`$**

A real matrix $A$ is diagonalizable over $`\mathbb{R}`$ **if and only if**:

* It has **3 linearly independent real eigenvectors**.

Thus:

* If all eigenvalues are **real and distinct**, it's **always diagonalizable** over $`\mathbb{R}`$.
* If some eigenvalues are complex, real diagonalization **may not** be possible.

---

### **5. Diagonalizing a Matrix Given Part of the Diagonalization**

If given partial data such as:

* A few eigenvalues and eigenvectors,
* A partially known matrix $P$ or $D$,

You can:

* Complete the missing eigenpairs by solving $`(A - \lambda I)\mathbf{v} = 0`$
* Complete $P$ and compute $`D = P^{-1} A P`$ or vice versa.

---

### **6. Full Example**

Let:

$$
A = \begin{bmatrix} 4 & 1 & 0 \\ 0 & 2 & 0 \\ 0 & 0 & 3 \end{bmatrix}
$$

#### Step 1: Characteristic Polynomial

$$
\det(A - \lambda I) = (4 - \lambda)(2 - \lambda)(3 - \lambda)
$$

Eigenvalues: $`\lambda\_1 = 4,\ \lambda\_2 = 2,\ \lambda\_3 = 3`$

#### Step 2: Eigenvectors

* $`\lambda\_1 = 4`$: $`\mathbf{v}\_1 = \begin{bmatrix} 1 \ 0 \ 0 \end{bmatrix}`$
* $`\lambda\_2 = 2`$: $`\mathbf{v}\_2 = \begin{bmatrix} -1 \ 2 \ 0 \end{bmatrix}`$
* $`\lambda\_3 = 3`$: $`\mathbf{v}\_3 = \begin{bmatrix} 0 \ 0 \ 1 \end{bmatrix}`$

#### Step 3: Form $P$ and $D$

$$
P = \begin{bmatrix} 1 & -1 & 0 \\ 0 & 2 & 0 \\ 0 & 0 & 1 \end{bmatrix}, \quad
D = \begin{bmatrix} 4 & 0 & 0 \\ 0 & 2 & 0 \\ 0 & 0 & 3 \end{bmatrix}
$$

Then:

$$
A = P D P^{-1}
$$

---

### **7. Summary Table**

| Task                                  | Key Idea                                                    |
| ------------------------------------- | ----------------------------------------------------------- |
| Diagonalizing a matrix                | $`A = P D P^{-1}`$ where $P$ has eigenvectors, $D$ has eigenvalues |
| Matrix with distinct eigenvalues      | Always diagonalizable                                       |
| Diagonalization with known eigenpairs | Assemble $P$, $D$, compute $`P^{-1}`$                       |
| Real diagonalizability check          | Requires 3 real, linearly independent eigenvectors          |
| Diagonalization with partial info     | Complete $P$ or $D$ using known data + eigenvalue equations |

---
