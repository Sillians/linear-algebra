## **Finding Complex Eigenvectors of Real 2×2 Matrices**

---

### **1. Overview: Complex Eigenvectors of Real Matrices**

For a real $`2 \times 2`$ matrix $A$, eigenvalues and eigenvectors may be complex when the characteristic 
polynomial has no real roots. If $`\lambda \in \mathbb{C} \setminus \mathbb{R}`$ is an eigenvalue of $A$, 
its complex conjugate $`\bar{\lambda}`$ is also an eigenvalue, and their corresponding eigenvectors $`\mathbf{v}`$ 
and $`\bar{\mathbf{v}}`$ are also complex conjugates.

---

### **2. Finding a Complex Eigenvalue of a Matrix Given a Complex Eigenvector**

Let $`A \in \mathbb{R}^{2 \times 2}`$, and suppose a complex eigenvector $`\mathbf{v} = \begin{bmatrix} a + bi \\ c + di \end{bmatrix}`$ is given. 
To find its eigenvalue:

#### **Step:**

Use the eigenvalue equation:

$`A\mathbf{v} = \lambda \mathbf{v} \Rightarrow \lambda = \frac{A\mathbf{v}}{\mathbf{v}} \text{ (interpreted component-wise)}`$

Pick one component (say the first) and solve:

$`(A\mathbf{v})_1 = \lambda \cdot v_1 \Rightarrow \lambda = \frac{(A\mathbf{v})_1}{v_1}`$

#### **Example:**

Given:

$`A = \begin{bmatrix} 0 & -1 \\ 1 & 0 \end{bmatrix}, \quad \mathbf{v} = \begin{bmatrix} 1 \\ i \end{bmatrix}`$

Then:

$`A\mathbf{v} = \begin{bmatrix} -i \\ 1 \end{bmatrix} \Rightarrow \lambda = \frac{-i}{1} = -i`$

---

### **3. Finding a Complex Eigenvector of a Matrix Given a Complex Eigenvalue**

Let $`\lambda \in \mathbb{C}`$ be a known eigenvalue of $`A \in \mathbb{R}^{2 \times 2}`$. 
To find a complex eigenvector $`\mathbf{v}`$:

#### **Step:**

Solve the system:

$`(A - \lambda I)\mathbf{v} = \mathbf{0}`$

This is a homogeneous linear system with complex coefficients. Choose one component freely (e.g., let $`x = 1`$) 
and solve for the other.

#### **Example:**

Given:

$`A = \begin{bmatrix} 2 & -5 \\ 1 & -2 \end{bmatrix}, \quad \lambda = i`$

Solve:

$`\left(\begin{bmatrix} 2 & -5 \\ 1 & -2 \end{bmatrix} - i \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix}\right) \begin{bmatrix} x \\ y \end{bmatrix} = 0 \Rightarrow \begin{bmatrix} 2 - i & -5 \\ 1 & -2 - i \end{bmatrix} \begin{bmatrix} x \\ y \end{bmatrix} = 0`$

Solving this gives the eigenvector:

$`\mathbf{v} = \begin{bmatrix} 5 \\ 2 - i \end{bmatrix}`$

---

### **4. Finding Two Linearly Independent Complex Eigenvectors of a 2×2 Matrix**

Since a $`2 \times 2`$ real matrix with complex eigenvalues always has a **conjugate pair of eigenvalues and eigenvectors**, 
we can construct two linearly independent complex eigenvectors as follows:

Let:

* $`\lambda = a + bi`$, with eigenvector $`\mathbf{v} = \begin{bmatrix} x + iy \\ z + iw \end{bmatrix}`$


* Then $`\bar{\lambda} = a - bi`$, with eigenvector $`\bar{\mathbf{v}} = \begin{bmatrix} x - iy \\ z - iw \end{bmatrix}`$


These two vectors are **linearly independent over $`\mathbb{C}`$** if $`b \ne 0`$.

#### **Example:**

Given:

$`A = \begin{bmatrix} 0 & -1 \\ 1 & 0 \end{bmatrix} \Rightarrow \text{Characteristic polynomial: } \lambda^2 + 1 = 0 \Rightarrow \lambda = i, -i`$

Eigenvectors:

* For $`i`$: $`\mathbf{v}_1 = \begin{bmatrix} 1 \\ i \end{bmatrix}`$


* For $`-i`$: $`\mathbf{v}_2 = \begin{bmatrix} 1 \\ -i \end{bmatrix}`$


These are linearly independent over $`\mathbb{C}`$.

---

### **Summary Table**

| Task                                         | Method                                                          |
| -------------------------------------------- | --------------------------------------------------------------- |
| **Find complex eigenvalue from eigenvector** | Use $`\lambda = \frac{(A\mathbf{v})_i}{v_i}`$                     |
| **Find eigenvector from complex eigenvalue** | Solve $`(A - \lambda I)\mathbf{v} = 0`$                           |
| **Find two complex eigenvectors**            | Use conjugate symmetry: $`\mathbf{v}, \bar{\mathbf{v}}`$          |
| **Eigenvalues of real 2x2 matrix**           | Conjugate pair if discriminant $`< 0`$                            |
| **Eigenvectors**                             | Complex conjugate pairs; linearly independent over $`\mathbb{C}`$ |

---

