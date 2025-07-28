## **The Gram-Schmidt Process for Two Vectors**

---

### **Overview**

The **Gram-Schmidt process** transforms a set of linearly independent vectors into an **orthogonal** (or orthonormal) 
set that spans the same subspace. For two vectors $`\mathbf{v}_1`$ and $`\mathbf{v}_2`$, 
the process outputs orthogonal vectors $`\mathbf{u}_1`$ and $`\mathbf{u}_2`$.

---

### **1. Gram-Schmidt Process for Two Vectors**

Given:

* Linearly independent vectors $`\mathbf{v}_1, \mathbf{v}_2 \in \mathbb{R}^n`$

#### Step-by-Step:

1. Set:

$$
\mathbf{u}_1 = \mathbf{v}_1
$$

2. Remove the component of $`\mathbf{v}_2`$ in the direction of $`\mathbf{u}_1`$:

$$
\mathbf{u}_2 = \mathbf{v}_2 - \frac{\mathbf{v}_2 \cdot \mathbf{u}_1}{\|\mathbf{u}_1\|^2} \mathbf{u}_1
$$

Now $`\mathbf{u}_1`$ and $`\mathbf{u}_2`$ are **orthogonal**.

To make them **orthonormal**:

$$
\mathbf{e}_1 = \frac{\mathbf{u}_1}{\|\mathbf{u}_1\|}, \quad \mathbf{e}_2 = \frac{\mathbf{u}_2}{\|\mathbf{u}_2\|}
$$

---

### **2. Finding an Orthogonal Basis for the Span of Two Vectors**

If $`\mathbf{v}_1, \mathbf{v}_2`$ span a subspace $`V \subseteq \mathbb{R}^n`$, then the orthogonal 
basis $`\{ \mathbf{u}_1, \mathbf{u}_2 \}`$ constructed by Gram-Schmidt satisfies:

$$
\text{Span}(\mathbf{v}_1, \mathbf{v}_2) = \text{Span}(\mathbf{u}_1, \mathbf{u}_2)
$$

---

### **3. Finding an Orthogonal Basis for the Column Space of a Matrix**

Given:

$$
A = \begin{bmatrix}
\mathbf{v}_1 & \mathbf{v}_2 & \cdots & \mathbf{v}_k
\end{bmatrix}
$$

Apply Gram-Schmidt to the **linearly independent** columns $`\mathbf{v}_1, \ldots, \mathbf{v}_k`$ of $A$ to obtain 
an orthogonal basis $`\{ \mathbf{u}_1, \ldots, \mathbf{u}_k \}`$ for $`\text{Col}(A)`$.

---

### **4. Finding an Orthonormal Basis of a Vector Space**

To find an **orthonormal basis**, normalize each orthogonal vector $`\mathbf{u}_i`$:

$$
\mathbf{e}_i = \frac{\mathbf{u}_i}{\|\mathbf{u}_i\|}
$$

Then $`\{ \mathbf{e}_1, \ldots, \mathbf{e}_k \}`$ is an orthonormal basis for the same subspace.

---

### **Example**

Let:

$$
\mathbf{v}_1 = \begin{pmatrix} 1 \\ 1 \end{pmatrix}, \quad \mathbf{v}_2 = \begin{pmatrix} 1 \\ -1 \end{pmatrix}
$$

Apply Gram-Schmidt:

1. $`\mathbf{u}_1 = \mathbf{v}_1 = \begin{pmatrix} 1 \\ 1 \end{pmatrix}`$

2. Project $`\mathbf{v}_2`$ onto $`\mathbf{u}_1`$:

$$
\text{proj}_{\mathbf{u}_1}(\mathbf{v}_2) = \frac{\mathbf{v}_2 \cdot \mathbf{u}_1}{\|\mathbf{u}_1\|^2} \mathbf{u}_1 = \frac{0}{2} \mathbf{u}_1 = \begin{pmatrix} 0 \\ 0 \end{pmatrix}
$$

3. $`\mathbf{u}_2 = \mathbf{v}_2 - \text{proj}_{\mathbf{u}_1}(\mathbf{v}_2) = \mathbf{v}_2`$

Thus:

$$
\mathbf{u}_1 = \begin{pmatrix} 1 \\ 1 \end{pmatrix}, \quad \mathbf{u}_2 = \begin{pmatrix} 1 \\ -1 \end{pmatrix}
$$

To get the orthonormal basis:

$$
\mathbf{e}_1 = \frac{1}{\sqrt{2}} \begin{pmatrix} 1 \\ 1 \end{pmatrix}, \quad \mathbf{e}_2 = \frac{1}{\sqrt{2}} \begin{pmatrix} 1 \\ -1 \end{pmatrix}
$$

---

### **Summary Table**

| Goal                       | Result                                           |
| -------------------------- | ------------------------------------------------ |
| **Orthogonal basis**       | Subtract projections from each subsequent vector |
| **Orthonormal basis**      | Normalize each orthogonal vector                 |
| **Basis for Column Space** | Apply Gram-Schmidt to independent columns        |
| **For two vectors**        | Use one projection and subtraction step          |

---

### **Key Properties**

* Orthogonal vectors: $`\mathbf{u}_i \cdot \mathbf{u}_j = 0`$ for $`i \ne j`$
* Orthonormal vectors: Also satisfy $`\|\mathbf{u}_i\| = 1`$
* Gram-Schmidt maintains the original span while improving numerical stability and interpretability

---

### **Use Cases**

* QR factorization
* Simplifying projections
* Solving least squares problems
* Constructing orthonormal bases for function spaces or subspaces in $`\mathbb{R}^n`$
