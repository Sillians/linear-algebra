## **Orthogonal Vectors in Euclidean Spaces**

In Euclidean space, **orthogonal vectors** are vectors that meet at a **right angle (90°)**. 
The concept of orthogonality is central in vector analysis, geometry, and linear algebra, 
especially in constructing orthonormal bases, solving least squares problems, and performing projections.

---

### **1. Identifying Orthogonal Vectors**

Two vectors $`\mathbf{u}, \mathbf{v} \in \mathbb{R}^n`$ are **orthogonal** if their **dot product is zero**:

$$
\boxed{\mathbf{u} \cdot \mathbf{v} = 0}
$$

This means they are **perpendicular** in space and share no directional component.

#### **Example:**

$$
\mathbf{u} = \langle 1, 2 \rangle, \quad \mathbf{v} = \langle 2, -1 \rangle
\Rightarrow \mathbf{u} \cdot \mathbf{v} = (1)(2) + (2)(-1) = 2 - 2 = 0
$$

So, $`\mathbf{u} \perp \mathbf{v}`$

---

### **2. Determining Components in Orthogonal Vectors**

To **construct a vector orthogonal** to a given vector, solve:

$$
\mathbf{u} \cdot \mathbf{v} = 0
$$

Assume all but one components and solve for the unknown that satisfies orthogonality.

#### **Example:**

Let $`\mathbf{v} = \langle 3, 4 \rangle`$. Find a vector $`\mathbf{u} = \langle a, b \rangle`$ orthogonal to $\mathbf{v}$.

Set:

$$
3a + 4b = 0 \Rightarrow a = -\frac{4}{3}b
$$

So one possible solution: $`\mathbf{u} = \langle -4, 3 \rangle`$

---

### **3. Calculating Dot Products Using Orthogonal Vectors**

If two vectors are orthogonal, their **dot product equals 0** — a useful shortcut.

#### **Example:**

$$
\mathbf{a} = \langle x, 2 \rangle, \quad \mathbf{b} = \langle 3, 1 \rangle
$$

Find $x$ so that $`\mathbf{a} \perp \mathbf{b}`$:

$$
x(3) + 2(1) = 0 \Rightarrow 3x + 2 = 0 \Rightarrow x = -\frac{2}{3}
$$

So:

$$
\mathbf{a} = \left\langle -\frac{2}{3}, 2 \right\rangle \text{ is orthogonal to } \mathbf{b}
$$

---

### **4. Determining a Vector Orthogonal to Two Given Vectors in $\mathbb{R}^3$**

If you’re given two vectors in 3D and need to find a vector orthogonal to **both**, use the **cross product**:

$$
\boxed{\mathbf{n} = \mathbf{u} \times \mathbf{v}}
$$

The resulting vector $`\mathbf{n}`$ is **orthogonal to both** $`\mathbf{u}`$ and $`\mathbf{v}`$.

#### **Example:**

Let $`\mathbf{u} = \langle 1, 0, 0 \rangle, \quad \mathbf{v} = \langle 0, 1, 0 \rangle`$

$$
\mathbf{u} \times \mathbf{v} = \begin{vmatrix}
\mathbf{i} & \mathbf{j} & \mathbf{k} \\
1 & 0 & 0 \\
0 & 1 & 0
\end{vmatrix} = \mathbf{k}
\Rightarrow \mathbf{n} = \langle 0, 0, 1 \rangle
$$


$`\mathbf{n}$ is orthogonal to both $\mathbf{u}$ and $\mathbf{v}`$

---

###  **Summary Table**

| Task                                | Method                                                                   |
| ----------------------------------- | ------------------------------------------------------------------------ |
| **Check orthogonality**             | $\mathbf{u} \cdot \mathbf{v} = 0$                                        |
| **Find missing component**          | Solve $\mathbf{u} \cdot \mathbf{v} = 0$                                  |
| **Dot product shortcut**            | If $\mathbf{u} \perp \mathbf{v}$, then $\mathbf{u} \cdot \mathbf{v} = 0$ |
| **Orthogonal to two vectors in 3D** | Use cross product: $\mathbf{u} \times \mathbf{v}$                        |

---

### **Conclusion**

Orthogonality gives structure to spaces — enabling clean **decompositions**, **projections**, 
and **basis constructions**. It's especially important in applications like orthonormal bases 
(e.g., Gram-Schmidt), vector projection, and solving systems with least squares. Identifying 
and constructing orthogonal vectors is a foundational skill in both theoretical and applied linear algebra.
