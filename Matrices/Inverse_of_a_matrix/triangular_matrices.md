### **Triangular Matrices**

---

### **1. What is a Triangular Matrix?**

A **triangular matrix** is a type of square matrix where **all entries either above or below the main diagonal are zero**.

There are two main types:

* **Upper Triangular Matrix**: All elements **below** the main diagonal are zero.

$$
U = \begin{bmatrix}
u_{11} & u_{12} & u_{13} \\
0      & u_{22} & u_{23} \\
0      & 0      & u_{33}
\end{bmatrix}
$$

* **Lower Triangular Matrix**: All elements **above** the main diagonal are zero.

$$
L = \begin{bmatrix}
l_{11} & 0      & 0      \\
l_{21} & l_{22} & 0      \\
l_{31} & l_{32} & l_{33}
\end{bmatrix}
$$

---

### **2. Key Properties of Triangular Matrices**

* **Determinant**: The determinant of a triangular matrix is the **product of its diagonal entries**.

  For a triangular matrix $T$:

$$
\det(T) = \prod_{i=1}^n t_{ii}
$$

* **Inverse**: The inverse of a triangular matrix (if it exists) is also triangular of the same type.

* **Eigenvalues**: The eigenvalues of a triangular matrix are exactly the **entries on its main diagonal**.

* **Stability in Computation**: Triangular matrices are easy to work with computationally. Many matrix algorithms (like LU decomposition) decompose a matrix into triangular forms.

---

### **3. Solving Linear Systems with Triangular Matrices**

If $A \mathbf{x} = \mathbf{b}$, and $A$ is triangular:

* **Forward substitution** (for lower triangular matrices): Start from the top.
* **Backward substitution** (for upper triangular matrices): Start from the bottom.

Example with lower triangular matrix:


$` \begin{bmatrix} 2 & 0 & 0 \\ 3 & 1 & 0 \\ 1 & -4 & 3 \end{bmatrix} \begin{bmatrix} x_1 \\ x_2 \\ x_3 \end{bmatrix} = \begin{bmatrix}  4 \\ 5 \\ -1  \end{bmatrix}`$

Solve using **forward substitution**:

* First row: $`2x_1 = 4 \Rightarrow x_1 = 2`$
* Second row: $`3x_1 + x_2 = 5 \Rightarrow 6 + x_2 = 5 \Rightarrow x_2 = -1`$
* Third row: $`x_1 - 4x_2 + 3x_3 = -1 \Rightarrow 2 + 4 + 3x_3 = -1 \Rightarrow x_3 = -7/3`$

---

### **4. Use in Matrix Decompositions**

Triangular matrices are essential in:

* **LU Decomposition**: Any square matrix (under certain conditions) can be written as:

$$
A = LU
$$

  Where $L$ is lower triangular and $U$ is upper triangular.

* **Cholesky Decomposition**: For symmetric positive-definite matrices:

$$
A = LL^T
$$

Where $L$ is lower triangular.

---

### **5. Summary**

* A triangular matrix has zeros either **above** (lower triangular) or **below** (upper triangular) the diagonal.
* They simplify matrix operations like solving systems, computing determinants, and decompositions.
* Their diagonal structure gives direct access to eigenvalues and determinant values.

Triangular matrices are fundamental in both theoretical and computational linear algebra due to their structured simplicity and numerical stability.
