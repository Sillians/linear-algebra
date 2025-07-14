## **The Intersection of Two Planes**

In 3D space, the intersection of two non-parallel, non-identical planes is typically a **line**. 
Understanding this intersection helps in visualizing geometry, solving systems of equations, 
and working with vector and parametric equations.

---

### **1. Identifying the Intersection of Two Planes**

Let two planes be given in Cartesian form:

* Plane 1: $`a_1x + b_1y + c_1z = d_1`$


* Plane 2: $`a_2x + b_2y + c_2z = d_2`$

To determine their intersection:

* If the planes are **parallel but not identical**, they have **no intersection**.


* If the planes are **identical**, their intersection is the **entire plane**.


* If the planes are **not parallel**, they intersect in a **line**.


To check if they’re parallel, compare their normal vectors:

$$
\mathbf{n}_1 = \langle a_1, b_1, c_1 \rangle, \quad
\mathbf{n}_2 = \langle a_2, b_2, c_2 \rangle
$$

If $`\mathbf{n}_1 \parallel \mathbf{n}_2`$, the planes are parallel.

---

### **2. Finding the Direction Vector of the Line of Intersection**

The **direction vector** $\mathbf{d}$ of the intersection line is **orthogonal to both plane normals**:

$$
\mathbf{d} = \mathbf{n}_1 \times \mathbf{n}_2
$$

This gives the direction in which both planes simultaneously “change” — the line’s direction.

#### **Example:**

Plane 1: $`x + y + z = 1$ → $\mathbf{n}_1 = \langle 1, 1, 1 \rangle`$
Plane 2: $`2x - y + z = 3$ → $\mathbf{n}_2 = \langle 2, -1, 1 \rangle`$

$$
\mathbf{d} = \mathbf{n}_1 \times \mathbf{n}_2 =
\begin{vmatrix}
\mathbf{i} & \mathbf{j} & \mathbf{k} \\
1 & 1 & 1 \\
2 & -1 & 1
\end{vmatrix}
= \langle 2, 1, -3 \rangle
$$

---

### **3. Finding the Vector Equation of the Line of Intersection**

To write the **vector equation**:

$$
\mathbf{r}(t) = \mathbf{r}_0 + t\mathbf{d}
$$

* $`\mathbf{d}`$: direction vector from the cross product above
* $`\mathbf{r}_0`$: a **point on both planes**, found by solving the two equations simultaneously

#### **Example (continued):**

From earlier:

* Plane 1: $`x + y + z = 1`$
* Plane 2: $`2x - y + z = 3`$

Let $z = 0$ (choose a value to simplify solving):

1. Plane 1: $`x + y = 1`$
2. Plane 2: $`2x - y = 3`$

Solving this system:

* From (1): $`y = 1 - x`$
* Plug into (2): $`2x - (1 - x) = 3 \Rightarrow 2x - 1 + x = 3 \Rightarrow 3x = 4 \Rightarrow x = \frac{4}{3}, y = \frac{-1}{3}, z = 0`$

So a point on both planes is:

$$
\mathbf{r}_0 = \left\langle \tfrac{4}{3}, \tfrac{-1}{3}, 0 \right\rangle
$$

Final vector equation of the line:

$$
\boxed{
\mathbf{r}(t) = \left\langle \tfrac{4}{3}, \tfrac{-1}{3}, 0 \right\rangle + t \langle 2, 1, -3 \rangle
}
$$

---

### Summary Table

| Task                                 | Method                                                                  |
| ------------------------------------ | ----------------------------------------------------------------------- |
| **Check if planes intersect**        | Compare normals: $\mathbf{n}_1$ vs. $\mathbf{n}_2$                      |
| **Direction vector of intersection** | $\mathbf{n}_1 \times \mathbf{n}_2$                                      |
| **Point on both planes**             | Solve system formed by both equations (use substitution or elimination) |
| **Vector equation of line**          | $\mathbf{r}(t) = \mathbf{r}_0 + t\mathbf{d}$                            |

---

### **Conclusion**

The intersection of two planes reveals how geometric surfaces interact in 3D space. 
By using cross products and systems of equations, you can find the precise **line of intersection**, 
which is essential in graphics, geometry, and multivariable calculus.
