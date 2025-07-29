## **The Spectral Theorem**

---

### **1. Overview of the Spectral Theorem**

The **Spectral Theorem** is a foundational result in linear algebra and functional analysis that provides conditions under which a matrix (or linear operator) 
can be diagonalized by an orthonormal basis of eigenvectors.

#### **Statement (Finite-Dimensional Real Case)**

If $`A \in \mathbb{R}^{n \times n}`$ is **symmetric**, then:

* All eigenvalues of $`A`$ are real.


* There exists an orthonormal basis of $`\mathbb{R}^n`$ consisting of eigenvectors of $`A`$.


* $`A`$ is **orthogonally diagonalizable**, i.e., there exists an orthogonal matrix $`Q`$ (with $`Q^\top Q = I`$) such that

$`A = Q \Lambda Q^\top,`$

  where $`\Lambda`$ is a diagonal matrix containing the real eigenvalues of $`A`$.

---

### **2. Identifying True Statements Regarding the Spectral Theorem**

| Statement                                                               | Truth Value | Explanation                                                                                                           |
| ----------------------------------------------------------------------- |-------------| --------------------------------------------------------------------------------------------------------------------- |
| Every symmetric matrix is diagonalizable.                               | ✅ True      | Symmetric matrices have an orthonormal basis of eigenvectors.                                                         |
| The eigenvalues of a symmetric matrix are always real.                  | ✅ True      | Follows directly from the Spectral Theorem.                                                                           |
| A real matrix is diagonalizable if and only if it is symmetric.         | ❌ False     | Diagonalizable matrices need not be symmetric (e.g., Jordan forms), but symmetric matrices are always diagonalizable. |
| The Spectral Theorem applies to all square matrices.                    | ❌ False     | It only applies to symmetric (real) or normal (complex) matrices.                                                     |
| A matrix is orthogonally diagonalizable if and only if it is symmetric. | ✅ True      | This is a defining characterization in the real case.                                                                 |

---

### **3. Finding the Spectral Decomposition of a Symmetric Matrix**

#### **Definition**

The **spectral decomposition** expresses a symmetric matrix $A$ as a sum of rank-one projections scaled by eigenvalues:


$`A = \sum_{i=1}^n \lambda_i \mathbf{u}_i \mathbf{u}_i^\top,`$


where $`\lambda_i`$ are the eigenvalues and $`\mathbf{u}_i`$ are the corresponding orthonormal eigenvectors.

#### **Example**

Let

$`A = \begin{bmatrix} 4 & 1 \\ 1 & 4 \end{bmatrix}.`$


**Step 1: Find eigenvalues**

Solve $`\det(A - \lambda I) = 0`$:

$`\begin{vmatrix} 4 - \lambda & 1 \\1 & 4 - \lambda \end{vmatrix} = (4 - \lambda)^2 - 1 = 0 \Rightarrow \lambda = 3, 5.`$


**Step 2: Find orthonormal eigenvectors**

* For $`\lambda = 5`$:
  Solve $`(A - 5I)\mathbf{v} = 0 \Rightarrow \mathbf{u}_1 = \frac{1}{\sqrt{2}}[1, 1]^\top`$.


* For $`\lambda = 3`$:
  Solve $`(A - 3I)\mathbf{v} = 0 \Rightarrow \mathbf{u}_2 = \frac{1}{\sqrt{2}}[1, -1]^\top`$.

**Step 3: Spectral decomposition**


$`A = 5 \mathbf{u}_1 \mathbf{u}_1^\top + 3 \mathbf{u}_2 \mathbf{u}_2^\top.`$

---

### **4. Finding a Projection Matrix That Orthogonally Projects a Vector to the Subspace Spanned by an Eigenvector**

#### **Definition**

Given a unit eigenvector $`\mathbf{u}`$, the **orthogonal projection** matrix onto the subspace spanned by $`\mathbf{u}`$ is:


$`P = \mathbf{u} \mathbf{u}^\top.`$


#### **Example**

Let $`\mathbf{u} = \frac{1}{\sqrt{2}} \begin{bmatrix} 1 \\ 1 \end{bmatrix}`$. Then:


$`P = \mathbf{u} \mathbf{u}^\top = \frac{1}{2} \begin{bmatrix} 1 \\ 1 \end{bmatrix} \begin{bmatrix} 1 & 1 \end{bmatrix} = \frac{1}{2} \begin{bmatrix} 1 & 1 \\ 1 & 1 \end{bmatrix}.`$


This matrix projects any vector $`\mathbf{x} \in \mathbb{R}^2`$ orthogonally onto the line spanned by $`\mathbf{u}`$.

---

### **Summary Table**

| Concept                        | Key Formula                                                 |
| ------------------------------ |-------------------------------------------------------------|
| Spectral Decomposition         | $`A = \sum \lambda_i \mathbf{u}_i \mathbf{u}_i^\top`$       |
| Orthogonal Projection          | $`P = \mathbf{u} \mathbf{u}^\top`$, for unit $`\mathbf{u}`$ |
| Orthogonal Diagonalization     | $`A = Q \Lambda Q^\top`$, $`Q`$ orthogonal                  |
| Condition for Spectral Theorem | Matrix is symmetric (real case)                             |

---
