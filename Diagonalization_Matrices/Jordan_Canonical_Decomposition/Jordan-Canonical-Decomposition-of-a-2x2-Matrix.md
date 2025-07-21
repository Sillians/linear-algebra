## **Jordan Canonical Decomposition of a 2×2 Matrix**

---

### **Overview**

The **Jordan canonical decomposition** (or Jordan normal form) rewrites a square matrix as:

$`A = PJP^{-1}`$

Where:

* $`A`$ is the original matrix.


* $`J`$ is the **Jordan form** — nearly diagonal with Jordan blocks.


* $`P`$ is the matrix of generalized eigenvectors.


For a **2×2 matrix**, Jordan form helps classify matrices that may not be diagonalizable and reveals their algebraic and geometric multiplicity structure.

---

### **Jordan Canonical Forms for 2×2 Matrices**

There are three cases for the Jordan canonical form of a 2×2 matrix:

#### **1. Two Distinct Eigenvalues**

If $`A`$ has two **distinct** eigenvalues $`\lambda_1 \ne \lambda_2`$, it is diagonalizable:


$`J = \begin{bmatrix} \lambda_1 & 0 \\0 & \lambda_2 \end{bmatrix}`$


Each eigenvalue has a corresponding **linearly independent** eigenvector. The matrix $`P`$ is composed of these eigenvectors.


#### **2. Scalar Matrix (All Eigenvalues Equal, Diagonal Matrix)**

If $`A = \lambda I`$, then:

$`J = \begin{bmatrix} \lambda & 0 \\0 & \lambda \end{bmatrix}`$


Here, the matrix is already diagonal and is its own Jordan form. Every vector is an eigenvector.

#### **3. One Eigenvalue (Non-Diagonalizable)**

If $A$ has **only one eigenvalue** $`\lambda`$ and is not diagonalizable:

$`J = \begin{bmatrix} \lambda & 1 \\0 & \lambda \end{bmatrix}`$

Only one linearly independent eigenvector exists; the second column of $P$ is a **generalized eigenvector**.

---

### **Finding Elements of Jordan Canonical Decomposition**


#### **Step 1: Compute the Eigenvalues**

Solve $`\det(A - \lambda I) = 0`$ to find the eigenvalues.


#### **Step 2: Determine Diagonalizability**

Check the dimension of each eigenspace. If it's less than the algebraic multiplicity, the matrix is **not diagonalizable**.


#### **Step 3: Find the Jordan Form $`J`$**

Choose the form (diagonal or Jordan block) depending on whether $`A`$ is diagonalizable.


#### **Step 4: Find the Matrix $`P`$**

* **First column**: An eigenvector of $A$.


* **Second column**:

  * If diagonalizable: another linearly independent eigenvector.


* If not diagonalizable: a generalized eigenvector satisfying:


$`(A - \lambda I)^2 \mathbf{v} = 0, \quad (A - \lambda I) \mathbf{v} \ne 0`$

---

### **Identifying Columns of a Transformation Matrix in a Jordan Decomposition**

The transformation matrix $`P`$ satisfies $`A = PJP^{-1}`$, where:

* Columns of $`P`$ are **(generalized) eigenvectors**.


* For non-diagonalizable cases, the chain:

$`(A - \lambda I)\mathbf{v}_2 = \mathbf{v}_1`$

---

### **Finding Elements of a Jordan Canonical Decomposition for a 2×2 Matrix**


#### **The First Column Case (Eigenvector)**

Given a matrix $`A`$ with eigenvalue $`\lambda`$, solve:

$`(A - \lambda I)\mathbf{v} = 0`$

to find the eigenvector (first column of $`P`$).

#### **The Second Column Case (Generalized Eigenvector)**

Solve:

$`(A - \lambda I)\mathbf{v}_2 = \mathbf{v}_1`$

to find a generalized eigenvector $`\mathbf{v}_2`$. This becomes the second column of $`P`$.

---

### **Example**

Let:

$`A = \begin{bmatrix} 5 & 1 \\0 & 5 \end{bmatrix}`$

* Eigenvalue: $`\lambda = 5`$


* One eigenvector: $`\mathbf{v}_1 = \begin{bmatrix} 1 \\ 0 \end{bmatrix}`$


* Generalized eigenvector: Solve $`(A - 5I)\mathbf{v}_2 = \mathbf{v}_1`$:


$`\begin{bmatrix} 0 & 1 \\0 & 0 \end{bmatrix} \begin{bmatrix} x \\y \end{bmatrix}= \begin{bmatrix} 1 \\0 \end{bmatrix} \Rightarrow y = 1, x \text{ arbitrary}`$


Pick $`x = 0`$, so $`\mathbf{v}_2 = \begin{bmatrix} 0 \\ 1 \end{bmatrix}`$


Then:


* $`P = \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix}`$


* $`J = \begin{bmatrix} 5 & 1 \\ 0 & 5 \end{bmatrix}`$

Hence, the Jordan decomposition is:

$`A = PJP^{-1}`$

---

### Summary Table

| Case                                        | Jordan Form $`J`$ | Matrix $`P`$ Columns                   |
| ------------------------------------------- | --------------- | ------------------------------------ |
| Two distinct eigenvalues                    | Diagonal        | Two eigenvectors                     |
| One repeated eigenvalue, diagonalizable     | Diagonal        | Two eigenvectors                     |
| One repeated eigenvalue, not diagonalizable | Jordan block    | Eigenvector, generalized eigenvector |

