## **Vectors in $\mathbb{R}^n$ — N-Dimensional Euclidean Space**

---

### **1. What Is $\mathbb{R}^n$?**

The space $`\mathbb{R}^n`$ is the set of all **n-tuples of real numbers** — it generalizes the 2D and 3D spaces to **n dimensions**.

A vector in $`\mathbb{R}^n`$ is written as:

$$
\mathbf{v} = \begin{bmatrix} v_1 \\ v_2 \\ \vdots \\ v_n \end{bmatrix}
\quad \text{or} \quad (v_1, v_2, \dots, v_n)
$$

This represents a **point or direction** in $n$-dimensional space.

---

### **2. Calculating a Multiple of a Vector**

If $`\mathbf{v} = (v_1, v_2, \dots, v_n)`$, and $`k \in \mathbb{R}`$, then:

$$
k\mathbf{v} = (kv_1, kv_2, \dots, kv_n)
$$

This **scales** the vector — stretching or compressing its magnitude.

**Example:**

$$
2 \cdot (3, -1, 4) = (6, -2, 8)
$$

---

### **3. Adding Multiples of Vectors**

If $\mathbf{u}, \mathbf{v} \in \mathbb{R}^n$, and $a, b \in \mathbb{R}$, then:

$$
a\mathbf{u} + b\mathbf{v} = (au_1 + bv_1, \, au_2 + bv_2, \dots, au_n + bv_n)
$$

This is a **linear combination** of the vectors.

**Example:**

Let $\mathbf{u} = (1, 2, 0)$, $\mathbf{v} = (3, -1, 4)$

$$
2\mathbf{u} + 3\mathbf{v} = 2(1, 2, 0) + 3(3, -1, 4) = (2, 4, 0) + (9, -3, 12) = (11, 1, 12)
$$

---

### **4. Calculating the Dot Product of Two Vectors**

The **dot product** (or inner product) of two vectors $\mathbf{u}, \mathbf{v} \in \mathbb{R}^n$ is:

$$
\mathbf{u} \cdot \mathbf{v} = u_1v_1 + u_2v_2 + \dots + u_nv_n
$$

It returns a **scalar**, and has geometric meaning:

$$
\mathbf{u} \cdot \mathbf{v} = \|\mathbf{u}\| \|\mathbf{v}\| \cos \theta
$$

Where $\theta$ is the angle between the vectors.

**Example:**

$$
\mathbf{u} = (1, 2, 3), \quad \mathbf{v} = (4, 0, -1) \Rightarrow \mathbf{u} \cdot \mathbf{v} = 1(4) + 2(0) + 3(-1) = 4 + 0 - 3 = 1
$$

---

### **5. Finding the Value of an Unknown Using the Dot Product**

If you are given:

$$
\mathbf{u} \cdot \mathbf{v} = c
$$

and some of the components of $\mathbf{u}$ or $\mathbf{v}$ are unknown, you can solve for the missing value by expanding the dot product.

**Example:**

Let $\mathbf{u} = (x, 2, -1)$, $\mathbf{v} = (1, 0, 4)$, and $\mathbf{u} \cdot \mathbf{v} = 3$.

Then:

$$
x(1) + 2(0) + (-1)(4) = 3 \Rightarrow x - 4 = 3 \Rightarrow x = 7
$$

---

### **Summary Table**

| Operation                 | Formula / Result                                                        |
| ------------------------- | ----------------------------------------------------------------------- |
| Scalar multiple of vector | $k\mathbf{v} = (kv_1, kv_2, \dots, kv_n)$                               |
| Linear combination        | $a\mathbf{u} + b\mathbf{v} = (au_i + bv_i)$                             |
| Dot product               | $\mathbf{u} \cdot \mathbf{v} = \sum u_iv_i$                             |
| Dot product (angle form)  | $\mathbf{u} \cdot \mathbf{v} = \|\mathbf{u}\|\|\mathbf{v}\|\cos \theta$ |
| Solving with dot product  | Expand and solve for unknown                                            |

---

### **Conclusion**

Vectors in $\mathbb{R}^n$ are the foundation of linear algebra and geometry in higher dimensions. Mastering scalar multiplication, linear combinations, and dot products is essential for deeper topics such as projections, orthogonality, and machine learning representations.
