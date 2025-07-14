## **The Components of a Vector with Respect to an Orthogonal or Orthonormal Basis**

---

### **1. Overview: Vector Components in an Orthogonal/Orthonormal Basis**

When a vector is expressed in terms of a **basis**, its **components** (coordinates) are the scalar weights applied 
to each basis vector. If the basis is **orthogonal** or **orthonormal**, we can compute these components efficiently 
using inner products.

---

### **2. Key Definitions**

| Term                      | Definition                                                                                                 |
| ------------------------- | ---------------------------------------------------------------------------------------------------------- |
| **Orthogonal Basis**      | A basis $`\{ \vec{u}_1, \vec{u}_2, \dots, \vec{u}_n \}`$ where $`\vec{u}_i \cdot \vec{u}_j = 0`$ for $`i \ne j`$ |
| **Orthonormal Basis**     | An orthogonal basis where each $`\| \vec{u}_i \| = 1`$                                                       |
| **Component** of a vector | Scalar projection of a vector onto a basis vector                                                          |

---

### **3. Decomposing a Vector in an Orthogonal Basis**

Let $`\vec{v} \in \mathbb{R}^n`$ and $`\{ \vec{u}_1, \dots, \vec{u}_k \}`$ be an **orthogonal** basis.

**Then** the component $`c_i`$ of $`\vec{v}`$ along $`\vec{u}_i`$ is:

$$
c_i = \frac{ \vec{v} \cdot \vec{u}_i }{ \| \vec{u}_i \|^2 }
$$

and the full decomposition is:

$$
\vec{v} = \sum_{i=1}^k \left( \frac{ \vec{v} \cdot \vec{u}_i }{ \| \vec{u}_i \|^2 } \right) \vec{u}_i
$$

---

### **4. Decomposing a Vector in an Orthonormal Basis**

Let $`\{ \vec{e}_1, \dots, \vec{e}_k \}`$ be an **orthonormal** basis. Then:

$$
\text{Component of } \vec{v} \text{ along } \vec{e}_i = \vec{v} \cdot \vec{e}_i
$$

And:

$$
\vec{v} = \sum_{i=1}^k (\vec{v} \cdot \vec{e}_i)\vec{e}_i
$$

This is simpler than the orthogonal case because $`\| \vec{e}_i \|^2 = 1`$.

---

### **5. Finding a Component of a Vector with Respect to a Given Orthogonal Basis**

**Given**:
$`\vec{v} \in \mathbb{R}^n`$
Orthogonal basis $`\{ \vec{u}_1, \vec{u}_2 \}`$

**Steps**:

1. Compute dot products: $`\vec{v} \cdot \vec{u}_i`$


2. Compute squared norms: $`\| \vec{u}_i \|^2`$


3. Get coefficients: $`c_i = \frac{ \vec{v} \cdot \vec{u}_i }{ \| \vec{u}_i \|^2 }`$


4. Reconstruct: $`\vec{v}_{\text{proj}} = \sum c_i \vec{u}_i`$

---

### **6. Calculating the Components of a Vector with Respect to a Given Orthonormal Basis**

**Given**:

* $`\vec{v} = [v_1, v_2, v_3]`$


* Orthonormal basis $`\{ \vec{e}_1, \vec{e}_2, \vec{e}_3 \}`$

**Steps**:

1. Compute each component:

$$
c_i = \vec{v} \cdot \vec{e}_i
$$

2. The vector in basis coordinates:

$$
[c_1, c_2, c_3]
$$

3. Reconstruction:

$$
\vec{v} = c_1 \vec{e}_1 + c_2 \vec{e}_2 + c_3 \vec{e}_3
$$

---

### **7. Example: Orthogonal Basis**

Let:

$$
\vec{v} = \begin{bmatrix} 3 \\ 1 \end{bmatrix},\quad
\vec{u}_1 = \begin{bmatrix} 1 \\ 0 \end{bmatrix},\quad
\vec{u}_2 = \begin{bmatrix} 0 \\ 2 \end{bmatrix}
$$

Note: $`\vec{u}_1 \cdot \vec{u}_2 = 0`$, so basis is orthogonal.

**Components**:

$$
c_1 = \frac{3(1) + 1(0)}{1^2 + 0^2} = 3,\quad
c_2 = \frac{3(0) + 1(2)}{0^2 + 2^2} = \frac{2}{4} = 0.5
$$

Thus,

$$
\vec{v} = 3 \vec{u}_1 + 0.5 \vec{u}_2
$$

---

### **8. Example: Orthonormal Basis**

Let:

$$
\vec{v} = \begin{bmatrix} 1 \\ 2 \end{bmatrix},\quad
\vec{e}_1 = \frac{1}{\sqrt{2}} \begin{bmatrix} 1 \\ 1 \end{bmatrix},\quad
\vec{e}_2 = \frac{1}{\sqrt{2}} \begin{bmatrix} -1 \\ 1 \end{bmatrix}
$$

**Components**:

$$
c_1 = \vec{v} \cdot \vec{e}_1 = \frac{1}{\sqrt{2}}(1 + 2) = \frac{3}{\sqrt{2}},\quad
c_2 = \vec{v} \cdot \vec{e}_2 = \frac{1}{\sqrt{2}}(-1 + 2) = \frac{1}{\sqrt{2}}
$$

**Thus**:

$$
\vec{v} = \frac{3}{\sqrt{2}} \vec{e}_1 + \frac{1}{\sqrt{2}} \vec{e}_2
$$

---

### **9. Summary Table**

| Basis Type  | Component Formula                                   | Simplicity | Requires Normalization? |
| ----------- | --------------------------------------------------- | ---------- | ----------------------- |
| Orthogonal  | $`\frac{\vec{v} \cdot \vec{u}_i}{\| \vec{u}_i \|^2}`$ | Moderate   | Yes                     |
| Orthonormal | $`\vec{v} \cdot \vec{e}_i`$                           | Simple     | No                      |

---

### **10. Final Tips**

* Always **verify orthogonality** with dot products.


* Use **orthonormal bases** for computational ease.


* Components w\.r.t. orthonormal bases are just dot products.


* With orthogonal bases, divide by $`\| \vec{u}_i \|^2`$.

---

This structure supports geometric understanding, efficient computation, and clarity in coordinate transformations.
