## **The Invertible Matrix Theorem (2×2 Case)**

---

### **1. What Is the Invertible Matrix Theorem?**

The **Invertible Matrix Theorem** states that for a square matrix, several fundamental properties are equivalent — they all either hold together (if the matrix is invertible) or fail together (if it's not).

In the context of a **$2 \times 2$** matrix:

$$
A = \begin{bmatrix} a & b \\ c & d \end{bmatrix}
$$

The matrix $A$ is **invertible** (also called **non-singular**) **if and only if** the following conditions hold.

---

### **2. Equivalent Conditions for Invertibility (2×2 Version)**

For a matrix $`A = \begin{bmatrix} a & b \\ c & d \end{bmatrix}`$, the following statements are **equivalent** — meaning they are all **true or all false**:

1. **$A$ is invertible**.
2. **The determinant of $A$ is nonzero**:

   $$
   \det(A) = ad - bc \ne 0
   $$
3. **The matrix equation $A\mathbf{x} = \mathbf{b}$ has a unique solution for every $\mathbf{b} \in \mathbb{R}^2$**.
4. **The system $A\mathbf{x} = \mathbf{0}$ has only the trivial solution $\mathbf{x} = \mathbf{0}$**.
5. **The columns of $A$ are linearly independent**.
6. **The columns of $A$ span $\mathbb{R}^2$**.
7. **$A$ has two pivot positions** (i.e., full rank).
8. **The inverse $A^{-1}$ exists and is given by**:

$$
A^{-1} = \frac{1}{\det(A)} \begin{bmatrix} d & -b \\ -c & a \end{bmatrix}
$$

9. **The transformation $T(\mathbf{x}) = A\mathbf{x}$** is **bijective** (both one-to-one and onto).

---

### **3. Example**

Let:

$$
A = \begin{bmatrix} 2 & 1 \\ 5 & 3 \end{bmatrix}
$$

Check if $A$ is invertible:

$$
\det(A) = (2)(3) - (1)(5) = 6 - 5 = 1 \ne 0
$$

✅ Since the determinant is non-zero, **all the above statements are true** — this matrix is invertible.

The inverse is:

$$
A^{-1} = \frac{1}{1} \begin{bmatrix} 3 & -1 \\ -5 & 2 \end{bmatrix} = \begin{bmatrix} 3 & -1 \\ -5 & 2 \end{bmatrix}
$$

---

### **4. Geometric Insight**

For $2 \times 2$ matrices:

* **Invertibility** means the transformation maps $\mathbb{R}^2$ onto itself without collapsing any area to zero.
* A nonzero determinant ensures the transformation preserves **dimension and orientation** (possibly with flipping or rotation), but not **flattening**.

---

### **5. Summary**

The **Invertible Matrix Theorem** for $2 \times 2$ matrices links core algebraic, geometric, and computational properties. If any one of the key conditions is true (like nonzero determinant), they **all are**. If even one fails, the matrix is **not invertible**. This interconnectedness is foundational in linear algebra.
