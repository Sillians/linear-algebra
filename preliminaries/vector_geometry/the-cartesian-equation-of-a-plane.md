## **The Cartesian Equation of a Plane**

A **plane** in 3D space can be described in various forms. One of the most widely used is 
the **Cartesian equation**, which captures the entire geometry of a plane using a **normal vector** 
and a **point on the plane**.

---

### **1. The Cartesian Equation of a Plane**

The **standard form** of the Cartesian equation of a plane is:

$$
ax + by + cz = d
$$

Where:

* $\mathbf{n} = \langle a, b, c \rangle$ is the **normal vector** to the plane,


* $(x, y, z)$ are the coordinates of any point on the plane,


* $d$ is a scalar determined using a known point on the plane.


Given a point $P_0 = (x_0, y_0, z_0)$, the Cartesian equation is:

$$
a(x - x_0) + b(y - y_0) + c(z - z_0) = 0
\Rightarrow ax + by + cz = ax_0 + by_0 + cz_0 = d
$$

---

### **2. Finding the Cartesian Equation of the Plane Perpendicular to a Given Vector**

If you're given:

* A **normal vector** $\mathbf{n} = \langle a, b, c \rangle$,


* A **point** $P_0 = (x_0, y_0, z_0)$,


The Cartesian equation is:

$$
a(x - x_0) + b(y - y_0) + c(z - z_0) = 0
$$

---

#### **Example:**

Normal vector $\mathbf{n} = \langle 2, -1, 3 \rangle$, Point $(1, 0, 2)$

$$
2(x - 1) - (y - 0) + 3(z - 2) = 0
\Rightarrow 2x - y + 3z = 8
$$

---

### **3. Finding the Cartesian Equation of the Plane Perpendicular to a Given Line**

A **line’s direction vector** acts as the **normal vector** for the plane **perpendicular** to it.

Given:

* Line direction vector $\mathbf{d} = \langle a, b, c \rangle$,


* Point on the plane $(x_0, y_0, z_0)$,

Use:

$$
a(x - x_0) + b(y - y_0) + c(z - z_0) = 0
$$

---

### **4. Finding the Vector Equation of a Plane Given Its Cartesian Equation**

Suppose you're given a plane equation:

$$
ax + by + cz = d
$$

Steps to convert to **vector form**:

* Identify **a point** $P_0$ on the plane (choose values that satisfy the equation).


* Find **two linearly independent vectors** $\mathbf{v}_1, \mathbf{v}_2$ that lie in the plane and are **orthogonal to the normal vector** $\mathbf{n} = \langle a, b, c \rangle$.


* Then the **vector equation** is:

$$
\mathbf{r}(s, t) = \mathbf{r}_0 + s\mathbf{v}_1 + t\mathbf{v}_2
$$

---

#### **Example:**

Plane: $x + y + z = 1$

Choose point $\mathbf{r}_0 = (1, 0, 0)$, normal $\mathbf{n} = \langle 1, 1, 1 \rangle$

Find $\mathbf{v}_1 = \langle 1, -1, 0 \rangle$, $\mathbf{v}_2 = \langle 1, 0, -1 \rangle$ (both orthogonal to $\mathbf{n}$)

Then:

$$
\mathbf{r}(s, t) = \langle 1, 0, 0 \rangle + s\langle 1, -1, 0 \rangle + t\langle 1, 0, -1 \rangle
$$

---

### **5. Finding the Cartesian Equation of the Plane Parallel to Two Vectors**

If two vectors $\mathbf{v}_1$ and $\mathbf{v}_2$ lie in the plane, then their **cross product** gives the **normal vector** to the plane:

$$
\mathbf{n} = \mathbf{v}_1 \times \mathbf{v}_2
$$

Once you find $\mathbf{n} = \langle a, b, c \rangle$ and a point $P_0 = (x_0, y_0, z_0)$, the Cartesian equation is:

$$
a(x - x_0) + b(y - y_0) + c(z - z_0) = 0
$$

---

#### **Example:**

Let $\mathbf{v}_1 = \langle 1, 0, 0 \rangle$, $\mathbf{v}_2 = \langle 0, 1, 1 \rangle$

$$
\mathbf{n} = \langle 0, -1, 1 \rangle
$$

Point: $(1, 1, 0)$

$$
0(x - 1) -1(y - 1) + 1(z - 0) = 0
\Rightarrow -y + 1 + z = 0 \Rightarrow z - y = -1
$$

Or:

$$
z - y + 1 = 0
$$

---

### Summary Table

| Task                                               | Method                                                            |
| -------------------------------------------------- | ----------------------------------------------------------------- |
| Cartesian equation of a plane with a normal vector | $a(x - x_0) + b(y - y_0) + c(z - z_0) = 0$                        |
| Plane ⟂ to a line                                  | Use the line’s direction vector as the normal                     |
| Vector → Cartesian form                            | Find normal via cross product of spanning vectors                 |
| Cartesian → vector form                            | Choose a point and find two spanning vectors orthogonal to normal |
| Plane ∥ to two vectors                             | Normal = $\mathbf{v}_1 \times \mathbf{v}_2$, use with point       |

---

Mastering these forms lets you switch between geometric and algebraic representations of planes — essential for solving problems in multivariable calculus, linear algebra, and 3D modeling.
