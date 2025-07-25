## **Block Diagonalization of $`n \times n`$ Matrices**

---

### **Overview of Block Diagonalization**

Block diagonalization refers to the process of converting a matrix $A \in \mathbb{R}^{n \times n}$ into a block diagonal matrix $B$ via a similarity transformation:

$$
A = PBP^{-1}
$$

where:

* $P$ is an invertible matrix.
* $B$ is block diagonal, typically with blocks that are simpler (e.g., scalar multiples, Jordan blocks, or invariant subspace matrices).

The motivation for block diagonalization is simplification—especially for computing powers of matrices, exponentials, or solving systems of equations.

---

### **1. Finding the Eigenvalues and Corresponding Eigenvectors of a Matrix in Block Diagonal Form**

If a matrix $A$ has been block diagonalized as:

$$
B = \begin{bmatrix}
B_1 & 0 & \cdots & 0 \\
0 & B_2 & \cdots & 0 \\
\vdots & \vdots & \ddots & \vdots \\
0 & 0 & \cdots & B_k
\end{bmatrix}
$$

Then:

* The **eigenvalues** of $A$ are the union of the eigenvalues of all blocks $B_i$.
* The **eigenvectors** of $A$ are constructed by embedding the eigenvectors of each $B_i$ into $\mathbb{R}^n$ by padding with zeros in non-relevant positions.

For instance, for block $B_1 \in \mathbb{R}^{2 \times 2}$, its eigenvector $\vec{v}_1 \in \mathbb{R}^2$ becomes $\tilde{\vec{v}}_1 = [v_1, v_2, 0, \dots, 0]^\top \in \mathbb{R}^n$.

---

### **2. Finding a Block Diagonalization of a 3×3 Matrix**

Let $A \in \mathbb{R}^{3 \times 3}$. If $A$ is diagonalizable or reducible to a block form, find:

* The eigenvalues $\lambda_1, \lambda_2, \lambda_3$
* The eigenvectors $\vec{v}_1, \vec{v}_2, \vec{v}_3$

Then form:

* $P = [\vec{v}_1 \ \vec{v}_2 \ \vec{v}_3]$
* $B = P^{-1} A P$

If $A$ has repeated eigenvalues or is defective, its block diagonal form may include Jordan blocks (non-diagonal upper-triangular blocks with 1s on the superdiagonal).

Example:
If $A$ has eigenvalues $2, 2, 3$ with only 2 linearly independent eigenvectors, then:

$$
B = \begin{bmatrix}
2 & 1 & 0 \\
0 & 2 & 0 \\
0 & 0 & 3
\end{bmatrix}
$$

---

### **3. Calculating the Invertible Matrix in Block Diagonal Form of a 3×3 Matrix**

To compute $P$ such that $A = P B P^{-1}$:

* Find a basis of generalized eigenvectors (i.e., solve $(A - \lambda I)^k \vec{v} = 0$) if defective.
* Stack these vectors column-wise into matrix $P$.
* Compute $B = P^{-1} A P$, which will be block diagonal.

---

### **4. Calculating the Invertible Matrix in Block Diagonal Form of an $n \times n$ Matrix**

The procedure generalizes:

1. **Find invariant subspaces** for each eigenvalue (generalized eigenspaces).
2. Construct a basis from vectors spanning each invariant subspace.
3. Assemble these bases into the columns of $P \in \mathbb{R}^{n \times n}$.
4. Use $P$ to obtain the block diagonal form $B$.

For **diagonalizable** matrices:

* $B$ will be diagonal.
* $P$ contains the eigenvectors of $A$.

For **non-diagonalizable** matrices:

* $B$ has Jordan blocks.
* $P$ contains generalized eigenvectors.

---

### **Summary Table**

| **Step**                                   | **Description**                                |
| ------------------------------------------ | ---------------------------------------------- |
| Find eigenvalues                           | Solve $\det(A - \lambda I) = 0$                |
| Find eigenvectors/generalized eigenvectors | Solve $(A - \lambda I)^k \vec{v} = 0$          |
| Construct $P$                              | Stack eigenvectors (or generalized) as columns |
| Compute $B$                                | $B = P^{-1} A P$, block diagonal               |
| Read off eigenspectrum                     | From diagonal or Jordan block form             |

Block diagonalization simplifies matrix analysis, especially in spectral theory, differential equations, and control systems.
