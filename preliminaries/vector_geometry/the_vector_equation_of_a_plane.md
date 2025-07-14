## **The Vector Equation of a Plane**

A **plane** in three-dimensional space can be described using vectors. The **vector equation of a 
plane** expresses all the points $\mathbf{r}$ that lie on the plane using:


* A **point on the plane** $\mathbf{r}_0$
* Two **non-parallel vectors** $\mathbf{v}_1$ and $\mathbf{v}_2$ that lie **in the plane**

---

### **1. General Vector Equation of a Plane**

If $\mathbf{r}_0$ is a point on the plane, and $\mathbf{v}_1$, $\mathbf{v}_2$ are two linearly independent vectors **in** the plane, then the vector equation of the plane is:

$$
\mathbf{r} = \mathbf{r}_0 + s \mathbf{v}_1 + t \mathbf{v}_2
$$

Where:

* $\mathbf{r}$ is the **position vector** of any point on the plane
* $s, t \in \mathbb{R}$ are scalar parameters

---

### **2. Finding the Vector Equation of the Plane Perpendicular to a Given Vector**

If a plane is **perpendicular to a vector** $`\mathbf{n}`$, then $`\mathbf{n}`$ is the **normal vector** to the plane.

Let $`\mathbf{r} = \begin{bmatrix} x \\ y \\ z \end{bmatrix}`$ and $`\mathbf{r}_0 = \begin{bmatrix} x_0 \\ y_0 \\ z_0 \end{bmatrix}`$ be a known point on the plane.

Then the plane satisfies:

$$
(\mathbf{r} - \mathbf{r}_0) \cdot \mathbf{n} = 0
$$

This is the **scalar form**, which ensures every point $`\mathbf{r}`$ lies on the plane by being orthogonal to $\mathbf{n}$.

---

### **3. Finding a Vector That Is Parallel To a Plane**

A vector is **parallel to a plane** if it is **orthogonal to the plane's normal vector**.

Let $`\mathbf{n}`$ be the plane’s normal vector. Then any vector $`\mathbf{v}`$ such that:

$$
\mathbf{v} \cdot \mathbf{n} = 0
$$

is **parallel to the plane**.

You can find such vectors by solving this dot product condition for $`\mathbf{v}`$.

---

### **4. Finding the Vector Equation of the Plane Perpendicular to a Given Straight Line**

If a plane is **perpendicular to a straight line**, then the direction vector of the line becomes the **normal vector** of the plane.

Let the line be given in vector form:

$$
\mathbf{r} = \mathbf{r}_1 + t\mathbf{d}
$$

Where $`\mathbf{d}`$ is the **direction vector** of the line.

To find the vector equation of the plane **perpendicular** to this line and passing through a point $\mathbf{r}_0$:


* Use $`\mathbf{d}`$ as the normal vector $`\mathbf{n}`$


* The equation becomes:

$$
(\mathbf{r} - \mathbf{r}_0) \cdot \mathbf{d} = 0
$$

Which is the scalar form of the plane?

You can also rewrite it in parametric/vector form by finding two vectors orthogonal to $`\mathbf{d}`$ and using them as the spanning vectors for the plane.

---

### **5. Summary**

| Scenario                                                  | Method                                                                             |
| --------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| General plane through a point with two spanning vectors   | $\mathbf{r} = \mathbf{r}_0 + s\mathbf{v}_1 + t\mathbf{v}_2$                        |
| Plane perpendicular to a vector $\mathbf{n}$              | $(\mathbf{r} - \mathbf{r}_0) \cdot \mathbf{n} = 0$                                 |
| Vector parallel to a plane with normal $\mathbf{n}$       | Find $\mathbf{v}$ such that $\mathbf{v} \cdot \mathbf{n} = 0$                      |
| Plane perpendicular to a line with direction $\mathbf{d}$ | Use $\mathbf{d}$ as the normal: $(\mathbf{r} - \mathbf{r}_0) \cdot \mathbf{d} = 0$ |

Understanding the vector equation of a plane is crucial for applications in geometry, computer graphics, and multivariable calculus, especially in defining surfaces and working with projections and intersections.
