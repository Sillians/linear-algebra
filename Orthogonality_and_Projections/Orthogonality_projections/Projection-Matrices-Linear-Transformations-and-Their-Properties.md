## **Projection Matrices, Linear Transformations, and Their Properties**

---

### **1. Overview: Projection as a Linear Transformation**

A **projection** is a linear transformation $`P: \mathbb{R}^n \to \mathbb{R}^n`$ that maps each vector onto a subspace $`W \subseteq \mathbb{R}^n`$ such that:


* $`P(\mathbf{v}) = \mathbf{v}`$ if $`\mathbf{v} \in W`$


* $`P(\mathbf{v}) \in W`$ for all $`\mathbf{v} \in \mathbb{R}^n`$


* $`\mathbf{v} - P(\mathbf{v}) \in W^\perp`$

---

### **2. Properties of Orthogonal Projection Matrices**

Let $`P \in \mathbb{R}^{n \times n}`$ be a **projection matrix**:


* **Idempotent**: $`P^2 = P`$


* **Symmetric** (for **orthogonal** projections): $`P^T = P`$


* All **eigenvalues** of $`P`$ are either 0 or 1


* Projects any vector onto a subspace $`W`$ such that:


$`\mathbf{v} = P\mathbf{v} + (I - P)\mathbf{v}, \quad \text{with } P\mathbf{v} \in W, \ (I - P)\mathbf{v} \in W^\perp`$


---

### **3. Finding a Matrix That Defines an Orthogonal Projection Onto the Subspace Spanned by a Vector**

Let $`\mathbf{u} \in \mathbb{R}^n`$, a nonzero vector. To project onto the subspace $`\mathrm{span}\{\mathbf{u}\}`$:


$`P = \frac{\mathbf{u}\mathbf{u}^T}{\mathbf{u}^T \mathbf{u}}`$


#### **Example**: If $`\mathbf{u} = \begin{bmatrix} 1 \\ 2 \end{bmatrix}`$, then:


$`P = \frac{1}{5} \begin{bmatrix} 1 \\ 2 \end{bmatrix} \begin{bmatrix} 1 & 2 \end{bmatrix}= \frac{1}{5} \begin{bmatrix} 1 & 2 \\2 & 4 \end{bmatrix}`$

---

### **4. Finding a Matrix That Defines an Orthogonal Projection Onto the Subspace Spanned by a Plane**

Suppose $`W \subseteq \mathbb{R}^n`$ is spanned by linearly independent vectors $`\mathbf{u}_1, \dots, \mathbf{u}_k`$. Let:

* $`A = [\mathbf{u}_1 \ \dots \ \mathbf{u}_k] \in \mathbb{R}^{n \times k}`$

Then the orthogonal projection matrix onto $`\mathrm{Col}(A)`$ is:


$`P = A(A^T A)^{-1}A^T`$


This generalizes the rank-1 projection formula from the previous section.

---

### **5. Identifying an Orthogonal Projection Matrix**

A matrix $`P \in \mathbb{R}^{n \times n}`$ is an **orthogonal projection** if and only if:

* $`P^2 = P`$ (idempotent)


* $`P^T = P`$ (symmetric)

If both hold, $`P`$ is a projection **onto** some subspace $`W`$ **orthogonally**.

---

### **6. Finding an Orthogonal Projection Matrix Given Vectors That Span the Orthogonal Complement**

Let $`W^\perp`$ be spanned by the columns of a matrix $`B \in \mathbb{R}^{n \times m}`$. Then, the orthogonal projection matrix onto $`W = (W^\perp)^\perp`$ is:


$`P = I - B(B^T B)^{-1} B^T`$


This projects orthogonally **onto the space orthogonal to the space spanned by the columns of $B$**.


#### **Explanation**:

* $`B(B^T B)^{-1}B^T`$ is the projection onto $`W^\perp`$


* Subtracting from the identity gives projection onto $`W`$

---

### **7. Summary Table**

| **Scenario**                         | **Projection Matrix $`P`$**                                |
|--------------------------------------|------------------------------------------------------------|
| Onto line spanned by $`\mathbf{u}`$  | $`\frac{\mathbf{u}\mathbf{u}^T}{\mathbf{u}^T \mathbf{u}}`$ |
| Onto subspace spanned by $`A`$       | $`A(A^T A)^{-1}A^T`$                                       |
| Onto subspace orthogonal to $`B`$    | $`I - B(B^T B)^{-1}B^T`$                                   |
| Orthogonal projection conditions     | $`P^2 = P`$, $`P^T = P`$                                   |

---

### **8. Applications**

* **Least Squares Approximation**: Finding closest point in a subspace


* **Data Decomposition**: PCA uses projection matrices


* **Control Theory** and **Signal Processing**: Filtering components orthogonal to noise

---

Projection matrices provide a powerful linear-algebraic mechanism to extract structure, enforce constraints, and analyze vector decomposition with respect to subspaces.
