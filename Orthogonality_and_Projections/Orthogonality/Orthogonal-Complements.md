## **Orthogonal Complements**

---

### **1. Overview of Orthogonal Complements**

The **orthogonal complement** of a subspace $`W \subseteq \mathbb{R}^n`$, denoted $`W^\perp`$, is the set of all vectors in $`\mathbb{R}^n`$ that are **orthogonal to every vector in $W$**.

Formally:

$$
W^\perp = \lbrace\{ \mathbf{v} \in \mathbb{R}^n \mid \mathbf{v} \cdot \mathbf{w} = 0 \text{ for all } \mathbf{w} \in W \rbrace\}
$$

**Key Properties**:

* $`W^\perp`$ is a **subspace** of $`\mathbb{R}^n`$


* $`\dim(W) + \dim(W^\perp) = n`$


* $`(W^\perp)^\perp = W`$ if $W$ is a subspace of $`\mathbb{R}^n`$

---

### **2. Identifying True Statements About Orthogonality**

Here are some fundamental **true statements** about orthogonality:

| Statement                                                                                               | Truth                                                 |
| ------------------------------------------------------------------------------------------------------- | ----------------------------------------------------- |
| If $`\mathbf{u} \cdot \mathbf{v} = 0`$, then $`\mathbf{u}`$ and $`\mathbf{v}`$ are orthogonal                 | ✅ True                                                |
| Every subspace $`W \subseteq \mathbb{R}^n`$ has an orthogonal complement $`W^\perp \subseteq \mathbb{R}^n`$ | ✅ True                                                |
| $`\mathbb{R}^n = W \oplus W^\perp`$ (direct sum of $W$ and $`W^\perp`$)                                     | ✅ True                                                |
| If $`\mathbf{v} \in W^\perp`$, then $`\mathbf{v} \cdot \mathbf{w} = 0`$ for **some** $\mathbf{w} \in W$     | ❌ False – must be true for **all** $`\mathbf{w} \in W`$ |
| A vector in $`W \cap W^\perp`$ must be the zero vector                                                    | ✅ True                                                |

---

### **3. Calculating the Components of a Vector Orthogonal to a Set**

Given a subspace $`W = \text{span}\{\mathbf{w}_1, \dots, \mathbf{w}_k\}`$, and a vector $`\mathbf{v} \in \mathbb{R}^n`$, 
the component of $`\mathbf{v}`$ that is **orthogonal to $W$** is:

$$
\mathbf{v}_\perp = \mathbf{v} - \text{proj}_W(\mathbf{v})
$$

Where:

$$
\text{proj}_W(\mathbf{v}) = A(A^TA)^{-1}A^T\mathbf{v}
$$

and $A$ is the matrix with columns $`\mathbf{w}_1, \dots, \mathbf{w}_k`$.

Then,

$$
\mathbf{v}_\perp = \mathbf{v} - A(A^TA)^{-1}A^T\mathbf{v}
$$

This is the orthogonal projection formula using **least squares**.

---

### **4. Identifying Which Vectors Belong to the Orthogonal Complement of a Set**

Given a set of vectors $`S = \{\mathbf{w}_1, \dots, \mathbf{w}_k\}`$, a vector $`\mathbf{v} \in \mathbb{R}^n`$ belongs to $`\text{span}(S)^\perp`$ **iff**:

$$
\mathbf{v} \cdot \mathbf{w}_i = 0 \quad \text{for all } i
$$

**Steps**:

1. Compute dot product: $`\mathbf{v} \cdot \mathbf{w}_i`$


2. If all dot products are zero ⇒ $`\mathbf{v} \in \text{span}(S)^\perp`$

#### **Example**:

Let $`S = \left\{ \begin{bmatrix}1\\2\end{bmatrix} \right\}`$

Check $`\mathbf{v} = \begin{bmatrix}2\\-1\end{bmatrix}`$:


$$
\mathbf{v} \cdot \begin{bmatrix}1\\2\end{bmatrix} = 2 \cdot 1 + (-1) \cdot 2 = 0 \Rightarrow \mathbf{v} \in S^\perp
$$



---

### **5. Finding the Orthogonal Complement of a Span**

Let $`W = \text{span}\{\mathbf{w}_1, \dots, \mathbf{w}_k\} \subseteq \mathbb{R}^n`$

To find $W^\perp$:

**Steps**:

1. Form a matrix $`A \in \mathbb{R}^{n \times k}`$ with columns $`\mathbf{w}_i`$


2. Solve the **homogeneous system** $`A^T\mathbf{x} = 0`$


3. The solution set is $`W^\perp`$

#### **Example**:

Let 

$$
W = \text{span} 
\left\lbrace 
\begin{bmatrix} 
1 \\ 1 \\ 0 
\end{bmatrix}, 
\begin{bmatrix} 
0 \\ 1 \\ 1 
\end{bmatrix} 
\right\rbrace
$$



Form matrix:

$$
A = \begin{bmatrix}
1 & 0 \\
1 & 1 \\
0 & 1
\end{bmatrix}
\Rightarrow
A^T = \begin{bmatrix}
1 & 1 & 0 \\
0 & 1 & 1
\end{bmatrix}
$$

Solve:

$`A^T\mathbf{x} = 0 \Rightarrow  \begin{bmatrix} 1 & 1 & 0 \\ 0 & 1 & 1  \end{bmatrix} \begin{bmatrix} x_1 \\ x_2 \\ x_3 \end{bmatrix} = \begin{bmatrix} 0 \\ 0 \end{bmatrix}`$

Equations:

* $`x_1 + x_2 = 0`$


* $`x_2 + x_3 = 0`$

Solution:

* $`x_2 = -x_1`$, $`x_3 = x_1`$

So:

$$
W^\perp = \text{span} \lbrace\{
\begin{bmatrix}
1 \\ -1 \\ 1
\end{bmatrix}
\rbrace\}
$$

---

### **Summary Table**

| **Task**                              | **Method**                                                               |
| ------------------------------------- | ------------------------------------------------------------------------ |
| Identify orthogonality properties     | Use dot product and subspace properties                                  |
| Compute orthogonal component          | Use $`\mathbf{v}_\perp = \mathbf{v} - \text{proj}_W(\mathbf{v})`$          |
| Verify if vector belongs to $`W^\perp`$ | Dot product must be zero with all basis vectors of $W$                   |
| Find orthogonal complement of a span  | Solve $`A^T\mathbf{x} = 0`$, where $A$ has the spanning vectors as columns |

