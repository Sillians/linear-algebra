## **Generalized Eigenvectors**

---

### **1. Overview: Generalized Eigenvectors**

In linear algebra, **generalized eigenvectors** arise when a matrix is **not diagonalizable**, i.e., when it does not have a full set of linearly independent eigenvectors. 
They help form a complete basis in such cases and play a key role in the **Jordan canonical form** of a matrix.


Given a square matrix $`A \in \mathbb{R}^{n \times n}`$ and an eigenvalue $`\lambda`$, a **generalized eigenvector** $`\mathbf{v}`$ of **rank** $k$ satisfies:

$`(A - \lambda I)^k \mathbf{v} = 0 \quad \text{but} \quad (A - \lambda I)^{k-1} \mathbf{v} \ne 0`$

---

### **2. Generalized Eigenvectors vs Regular Eigenvectors**

| Concept        | Regular Eigenvector                                          | Generalized Eigenvector                                 |
| -------------- |--------------------------------------------------------------|---------------------------------------------------------|
| Condition      | $`(A - \lambda I)\mathbf{v} = 0`$                            | $`(A - \lambda I)^k \mathbf{v} = 0`$ for some $`k > 1`$ |
| When it exists | Always for every eigenvalue (up to algebraic multiplicity)   | When matrix is not diagonalizable                       |
| Rank           | 1                                                            | ≥ 2                                                     |
| Use            | Diagonalization                                              | Jordan form or solving differential systems             |


---

### **3. Identifying Generalized Eigenvectors of a 2×2 Matrix**

#### **Example**

Let

$`A = \begin{bmatrix} 4 & 1 \\0 & 4 \end{bmatrix}`$


1. **Eigenvalues**:
   Solve $`\det(A - \lambda I) = 0`$

$`\det\begin{bmatrix} 4 - \lambda & 1 \\0 & 4 - \lambda \end{bmatrix} = (4 - \lambda)^2 = 0 \Rightarrow \lambda = 4 \ \text{(algebraic multiplicity 2)}`$



2. **Find regular eigenvectors**:


$`(A - 4I) = \begin{bmatrix} 0 & 1 \\0 & 0 \end{bmatrix} \Rightarrow \begin{bmatrix} 0 & 1 \\0 & 0 \end{bmatrix} \begin{bmatrix} x \\y \end{bmatrix} = 0 \Rightarrow y = 0 \Rightarrow \text{Eigenvector: } \mathbf{v}_1 = \begin{bmatrix}1 \\ 0\end{bmatrix}`$

Only 1 linearly independent eigenvector ⇒ **not diagonalizable**.



3. **Find generalized eigenvector** $`\mathbf{v}_2`$:

Solve:

$`(A - 4I)\mathbf{v}_2 = \mathbf{v}_1 = \begin{bmatrix}1 \\ 0\end{bmatrix}`$

That is:

$`\begin{bmatrix} 0 & 1 \\0 & 0 \end{bmatrix} \begin{bmatrix} x \\y \end{bmatrix}= \begin{bmatrix} y \\0 \end{bmatrix}= \begin{bmatrix} 1 \\0 \end{bmatrix} \Rightarrow y = 1`$

Choose $`x = 0`$, then generalized eigenvector:

$`\mathbf{v}_2 = \begin{bmatrix}0 \\ 1\end{bmatrix}`$

Verify:

* $`(A - 4I)\mathbf{v}_2 = \mathbf{v}_1`$
* $`(A - 4I)^2 \mathbf{v}_2 = 0`$

---

### **4. Identifying Generalized Eigenvectors Using the Definition**

Given:

$`(A - \lambda I)^k \mathbf{v} = 0 \quad \text{but} \quad (A - \lambda I)^{k-1} \mathbf{v} \ne 0`$

To identify a generalized eigenvector:

* First compute $`N_k = \ker\left((A - \lambda I)^k\right)`$
* Compare with $`N_{k-1}`$
* The new vectors in $`N_k \setminus N_{k-1}`$ are generalized eigenvectors of **rank $k$**


---

### **5. Identifying Generalized Eigenvectors of a 3×3 Matrix**

#### **Example**

Let

$`A = \begin{bmatrix} 2 & 1 & 0 \\0 & 2 & 1 \\0 & 0 & 2 \end{bmatrix}`$


This is an **upper-triangular matrix**, so all eigenvalues are 2 (algebraic multiplicity 3).

1. **Eigenvectors**:
   Solve $`(A - 2I)\mathbf{v} = 0`$

$`A - 2I = \begin{bmatrix} 0 & 1 & 0 \\0 & 0 & 1 \\0 & 0 & 0 \end{bmatrix} \Rightarrow \mathbf{v}_1 = \begin{bmatrix}1 \\ 0 \\ 0\end{bmatrix}`$


Only one eigenvector ⇒ need 2 generalized eigenvectors to get 3-dimensional basis.

2. **First Generalized Eigenvector** $`\mathbf{v}_2`$:

Solve:

$`(A - 2I)\mathbf{v}_2 = \mathbf{v}_1 = \begin{bmatrix}1 \\ 0 \\ 0\end{bmatrix} \Rightarrow \mathbf{v}_2 = \begin{bmatrix}0 \\ 1 \\ 0\end{bmatrix}`$

Verify:

$`(A - 2I)\mathbf{v}_2 = \mathbf{v}_1, \quad (A - 2I)^2 \mathbf{v}_2 = 0`$


3. **Second Generalized Eigenvector** $`\mathbf{v}_3`$:


$`(A - 2I)\mathbf{v}_3 = \mathbf{v}_2 = \begin{bmatrix}0 \\ 1 \\ 0\end{bmatrix} \Rightarrow \mathbf{v}_3 = \begin{bmatrix}0 \\ 0 \\ 1\end{bmatrix}`$


So we form a **Jordan chain**:


$`(A - 2I)\mathbf{v}_3 = \mathbf{v}_2, \quad (A - 2I)\mathbf{v}_2 = \mathbf{v}_1, \quad (A - 2I)\mathbf{v}_1 = 0`$

---

### **6. Summary Table**

| Matrix               | Eigenvalue $`\lambda`$           | Regular Eigenvectors | Generalized Eigenvectors |
| -------------------- |----------------------------------| -------------------- | ------------------------ |
| $2\times2$ defective | 1 eigenvalue (mult 2), 1 eigvec  | 1                    | 1                        |
| $3\times3$ defective | 1 eigenvalue (mult 3), 1 eigvec  | 1                    | 2                        |

---

### **7. Application: Jordan Canonical Form**

Generalized eigenvectors allow constructing a **Jordan basis**, which transforms a matrix $A$ into its **Jordan form**:


$`J = P^{-1} A P = \begin{bmatrix} \lambda & 1 & 0 \\0 & \lambda & 1 \\0 & 0 & \lambda \end{bmatrix}`$


This helps in computing functions of matrices, solving systems of ODEs, and analyzing stability.

---

### ✅ Key Insight

Generalized eigenvectors fill the gap when a matrix is **not diagonalizable** by extending the eigenspace to the full dimension needed for a basis via **Jordan chains**.
