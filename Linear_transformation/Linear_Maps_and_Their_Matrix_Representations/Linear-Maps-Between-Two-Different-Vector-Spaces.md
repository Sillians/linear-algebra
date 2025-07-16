## **Linear Maps Between Two Different Vector Spaces**

---

### **1. What Is a Linear Map?**

A **linear map** (or linear transformation) between two vector spaces $V$ and $W$ over the same field $`\mathbb{F}`$ is a function:

$`T: V \rightarrow W`$

that satisfies:

* **Additivity**: $`T(u + v) = T(u) + T(v)`$


* **Homogeneity**: $`T(cu) = cT(u)`$


for all $`u, v \in V`$, and all scalars $`c \in \mathbb{F}`$.

---

### **2. Standard Matrix of a Linear Transformation**

If $`T: \mathbb{R}^n \rightarrow \mathbb{R}^m`$ is linear, it can be represented by **matrix multiplication**:

$`T(\mathbf{x}) = A\mathbf{x}`$

where $`A \in \mathbb{R}^{m \times n}`$ is the **standard matrix** of the transformation.

---

#### **Finding the Standard Matrix:**

To find $A$, apply $T$ to each **standard basis vector** $`\mathbf{e}_i \in \mathbb{R}^n`$:

$`A = \begin{bmatrix} T(\mathbf{e}_1) & T(\mathbf{e}_2) & \cdots & T(\mathbf{e}_n) \end{bmatrix}`$

---

#### **Example:**

Let $`T: \mathbb{R}^2 \to \mathbb{R}^2`$ be defined by:

$`T\left(\begin{bmatrix} x \\ y \end{bmatrix}\right) = \begin{bmatrix} 3x + y \\ x - 2y \end{bmatrix}`$

Then:

* $`T(\mathbf{e}_1) = T\left(\begin{bmatrix}1\\0\end{bmatrix}\right) = \begin{bmatrix} 3 \\ 1 \end{bmatrix}`$
* $`T(\mathbf{e}_2) = T\left(\begin{bmatrix}0\\1\end{bmatrix}\right) = \begin{bmatrix} 1 \\ -2 \end{bmatrix}`$

So, the **standard matrix** is:

$`A = \begin{bmatrix} 3 & 1 \\ 1 & -2 \end{bmatrix}`$

---

### **3. Determining the Components of a Linear Map**

If $`T: V \rightarrow W`$, and both spaces have **bases**:

* $`\mathcal{B}_V = \{v_1, \dots, v_n\}`$
* $`\mathcal{B}_W = \{w_1, \dots, w_m\}`$

Then each $`T(v_i)`$ can be written as a linear combination of the $`w_j`$’s:

$`T(v_i) = \sum_{j=1}^m a_{ji} w_j`$

These coefficients $`a_{ji}`$ form the **matrix representation** of $T$ with respect to those bases.

---

### **4. Finding the Image of a Vector Under a Linear Map**

To compute $`T(\mathbf{x})`$:

1. Express $`\mathbf{x}`$ as a coordinate vector (if needed).
2. Multiply by the standard matrix $A$:

$`T(\mathbf{x}) = A\mathbf{x}`$

---

#### **Example:**

Given $`A = \begin{bmatrix} 3 & 1 \\ 1 & -2 \end{bmatrix}`$ and $`\mathbf{x} = \begin{bmatrix} 4 \\ 2 \end{bmatrix}`$, compute:

$`T(\mathbf{x}) = A \mathbf{x} = \begin{bmatrix} 3 \cdot 4 + 1 \cdot 2 \\  1 \cdot 4 + (-2) \cdot 2 \end{bmatrix} = \begin{bmatrix} 14 \\0 \end{bmatrix}`$

So, the **image** of $`\mathbf{x}`$ under $T$ is $`\begin{bmatrix} 14 \\ 0 \end{bmatrix}`$.

---

### ✅ **Summary**

| Concept         | Description                                                      |
| --------------- |------------------------------------------------------------------|
| Linear Map      | A structure-preserving function between vector spaces            |
| Standard Matrix | Formed by applying $T$ to standard basis vectors                 |
| Components      | Coefficients from expressing $`T(v_i)`$ in terms of basis of $W$ |
| Image           | The result of applying $T$ to a vector $`\mathbf{x}`$            |

---

### Applications

* Coordinate changes
* Transformations in graphics
* Solving systems of equations
* Feature maps in machine learning
