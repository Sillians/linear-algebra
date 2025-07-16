## **Finding the Canonical Form of a Quadratic Form Using Orthogonal Transformations**

---

### **1. Overview of Quadratic Forms**

A **quadratic form** on $`\mathbb{R}^n`$ is a scalar-valued function defined as:

$`Q(\mathbf{x}) = \mathbf{x}^\top A \mathbf{x}`$

where:

* $`\mathbf{x} \in \mathbb{R}^n`$


* $`A \in \mathbb{R}^{n \times n}`$ is a **symmetric** matrix

---

### **2. Goal: Canonical Form**

The **canonical form** of a quadratic function is one where cross-product terms vanish. Using an **orthogonal transformation**, this is achieved by diagonalizing the symmetric matrix $A$.

If $P$ is an orthogonal matrix such that:

$`P^\top A P = D`$

where $D$ is diagonal, then:

$`Q(\mathbf{x}) = \mathbf{x}^\top A \mathbf{x} = \mathbf{y}^\top D \mathbf{y} \quad \text{with } \mathbf{y} = P^\top \mathbf{x}`$

---

### **3. Finding the Canonical Form by Finding Eigenvalues**

To find the canonical form:

1. Find **eigenvalues and eigenvectors** of the symmetric matrix $A$


2. Construct an orthogonal matrix $P$ whose columns are **orthonormal eigenvectors** of $A$


3. Compute the diagonal matrix $`D = P^\top A P`$


Each diagonal entry of $D$ corresponds to a coefficient in the canonical form:

$`Q(\mathbf{x}) = \lambda_1 y_1^2 + \lambda_2 y_2^2 + \dots + \lambda_n y_n^2`$

---

### **4. Reducing a 2D Quadratic Function**

#### **Example:**

$`Q(x, y) = 4x^2 + 4xy + y^2`$

**Step 1: Write the matrix form**:

$`A = \begin{bmatrix} 4 & 2 \\2 & 1 \end{bmatrix}`$



**Step 2: Find eigenvalues** by solving $`\det(A - \lambda I) = 0`$:

$`\lambda^2 - 5\lambda = 0 \Rightarrow \lambda = 0, 5`$



**Step 3: Find orthonormal eigenvectors** $`\mathbf{u}_1, \mathbf{u}_2`$



**Step 4: Construct orthogonal matrix** $`P = [\mathbf{u}_1\ \mathbf{u}_2]`$



**Step 5: Compute**:

$`D = P^\top A P = \begin{bmatrix} 0 & 0 \\0 & 5 \end{bmatrix} \Rightarrow Q(\mathbf{x}) = 0 \cdot y_1^2 + 5 \cdot y_2^2`$



This is the **canonical form**.

---

### **5. Reducing a 3D Quadratic Function**

Given:

$`Q(x, y, z) = x^2 + 2xy + 3y^2 + 4xz + 2yz + z^2`$


**Step 1: Write symmetric matrix** $A$:

$`A = \begin{bmatrix} 1 & 1 & 2 \\1 & 3 & 1 \\2 & 1 & 1 \end{bmatrix}`$



**Step 2: Find eigenvalues and orthonormal eigenvectors**

* Solve $`\det(A - \lambda I) = 0`$ to find $`\lambda_1, \lambda_2, \lambda_3`$
* Let $`P = [\mathbf{u}_1\ \mathbf{u}_2\ \mathbf{u}_3]`$



**Step 3: Compute** $`D = P^\top A P`$

Canonical form:

$`Q(x, y, z) = \lambda_1 y_1^2 + \lambda_2 y_2^2 + \lambda_3 y_3^2`$

---

### ✅ **Summary Table**

| Step | Action                                                                          |
| ---- |---------------------------------------------------------------------------------|
| 1    | Write $`Q(\mathbf{x}) = \mathbf{x}^\top A \mathbf{x}`$, ensure $A$ is symmetric |
| 2    | Find eigenvalues and orthonormal eigenvectors of $A$                            |
| 3    | Form orthogonal matrix $P$, with eigenvectors as columns                        |
| 4    | Diagonalize: $`P^\top A P = D`$                                                 |
| 5    | Rewrite quadratic form as $`Q(\mathbf{x}) = \mathbf{y}^\top D \mathbf{y}`$      |

---

### **Applications**

* Classifying critical points (optimization, saddle points)
* Principal component analysis (PCA)
* Conic sections and quadric surfaces
* Rotating coordinate systems to simplify problems
