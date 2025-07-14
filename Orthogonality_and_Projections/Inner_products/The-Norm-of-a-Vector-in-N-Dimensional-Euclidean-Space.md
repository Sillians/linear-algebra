## **The Norm of a Vector in N-Dimensional Euclidean Space**

The **norm** of a vector measures its **length** or **magnitude** in space. In $\mathbb{R}^n$, 
it generalizes the notion of distance from the origin and forms the basis for concepts like distance, direction, unit vectors, and orthogonality.

---

### **1. Calculating the Norm of a Vector**

The **norm** (or **Euclidean norm**) of a vector $`\mathbf{v} = \langle v_1, v_2, \dots, v_n \rangle`$ is defined as:

$$
\boxed{\|\mathbf{v}\| = \sqrt{v_1^2 + v_2^2 + \dots + v_n^2}}
$$

This is also known as the **2-norm** or **$\ell_2$ norm**.

#### **Example:**

$$
\mathbf{v} = \langle 3, -4, 1 \rangle
\Rightarrow \|\mathbf{v}\| = \sqrt{3^2 + (-4)^2 + 1^2} = \sqrt{9 + 16 + 1} = \sqrt{26}
$$

---

### **2. Finding the Distance Between Two Vectors**

The **distance** between vectors $\mathbf{u}$ and $\mathbf{v}$ in $\mathbb{R}^n$ is the **norm of their difference**:

$$
\boxed{\text{Distance} = \|\mathbf{u} - \mathbf{v}\|}
$$

#### **Example:**

$$
\mathbf{u} = \langle 1, 2 \rangle, \quad \mathbf{v} = \langle 4, 6 \rangle
\Rightarrow \mathbf{u} - \mathbf{v} = \langle -3, -4 \rangle
\Rightarrow \|\mathbf{u} - \mathbf{v}\| = \sqrt{9 + 16} = \sqrt{25} = 5
$$

---

### **3. Factoring a Constant Out of the Norm**

If $c \in \mathbb{R}$, and $\mathbf{v} \in \mathbb{R}^n$, then:

$$
\boxed{\|c\mathbf{v}\| = |c| \cdot \|\mathbf{v}\|}
$$

The norm scales linearly with the **absolute value** of the scalar.

#### **Example:**

$$
\mathbf{v} = \langle 2, 3 \rangle, \quad c = -2
\Rightarrow \| -2\mathbf{v} \| = |-2| \cdot \|\langle 2, 3 \rangle\| = 2 \cdot \sqrt{13}
$$

---

### **4. Normalizing a Vector**

To **normalize** a vector means to convert it to a **unit vector** (a vector with norm 1) pointing in the **same direction**:

$$
\boxed{\mathbf{u} = \frac{\mathbf{v}}{\|\mathbf{v}\|}}
$$

This is often used in direction-based calculations (like projection, angles, or basis formation).

#### **Example:**

$$
\mathbf{v} = \langle 3, 4 \rangle \Rightarrow \|\mathbf{v}\| = 5
\Rightarrow \text{Unit vector: } \frac{1}{5} \langle 3, 4 \rangle = \langle \tfrac{3}{5}, \tfrac{4}{5} \rangle
$$

---

### ✅ **Summary Table**

| Concept                                   | Formula / Rule                                                 |  
| ----------------------------------------- |----------------------------------------------------------------| 
| Norm of $\mathbf{v} \in \mathbb{R}^n$     | $\|\mathbf{v}\| = \sqrt{\sum v_i^2}$                           |  
| Distance between $\mathbf{u}, \mathbf{v}$ | $\|\mathbf{u} - \mathbf{v}\|$                                  |   
| Scalar multiple inside norm               | $`( \|c\mathbf{v}\| = \mid c \mid \|\mathbf{v}\| )`$           |
| Normalized (unit) vector                  | $\mathbf{v}_{\text{unit}} = \frac{\mathbf{v}}{\|\mathbf{v}\|}$ | 

---

### **Conclusion**

The norm is a central tool for understanding **magnitude, distance, scaling, and direction** in Euclidean space. 
It's essential in applications across geometry, physics, optimization, and machine learning — anywhere that the shape or direction of data matters.
