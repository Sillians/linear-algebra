## **The Image of an Affine Transformation**

An **affine transformation** maps geometric objects such as points, lines, and polygons to 
new positions in space through a combination of **linear transformation** and **translation**.
The result of applying this transformation is called the **image** of the object.

The general form of an affine transformation is:

$$
T(\mathbf{x}) = A\mathbf{x} + \mathbf{b}
$$

Where:

* $`A`$ is a matrix representing a **linear transformation** (rotation, scaling, shear)


* $`\mathbf{b}`$ is a **translation vector**

---

### **1. Finding the Image of a Point or Segment**

To find the image of a **point** $`\mathbf{x}`$, simply apply the transformation:

$$
T(\mathbf{x}) = A\mathbf{x} + \mathbf{b}
$$

#### **Example:**

Let $`A = \begin{bmatrix} 2 & 0 \\ 0 & 3 \end{bmatrix}`$, $`\mathbf{b} = \begin{bmatrix} 1 \\ -1 \end{bmatrix}`$, and $`\mathbf{x} = \begin{bmatrix} 4 \\ 1 \end{bmatrix}`$.

Then:

$$
T(\mathbf{x}) = \begin{bmatrix} 2 & 0 \\ 0 & 3 \end{bmatrix} \begin{bmatrix} 4 \\ 1 \end{bmatrix} + \begin{bmatrix} 1 \\ -1 \end{bmatrix}
= \begin{bmatrix} 8 \\ 3 \end{bmatrix} + \begin{bmatrix} 1 \\ -1 \end{bmatrix}
= \begin{bmatrix} 9 \\ 2 \end{bmatrix}
$$

To find the image of a **line segment**, apply the transformation to **both endpoints** and connect the resulting points.

---

### **2. Finding the Image of a Polygon Under an Affine Transformation**

To transform a polygon:

* Apply $`T(\mathbf{x}) = A\mathbf{x} + \mathbf{b}`$ to **each vertex** of the polygon.
* Connect the resulting transformed vertices in order.

Affine transformations preserve:

* **Straightness** (lines map to lines),


* **Parallelism** (parallel lines remain parallel),


* But not necessarily **lengths** or **angles**.

---

### **3. Determining Whether an Affine Transformation is Orientation-Preserving**

The **orientation** of an affine transformation depends on the **determinant** of matrix $A$:

* If $`\det(A) > 0`$: The transformation is **orientation-preserving**


* If $`\det(A) < 0`$: The transformation **reverses orientation**


* If $`\det(A) = 0`$: The transformation is **degenerate** (collapses space)

---

### **4. Determining the Area Scale Factor of an Affine Transformation**

The **area scale factor** of an affine transformation is given by:

$$
\text{Area Scale Factor} = |\det(A)|
$$

This tells you how much the transformation **scales the area** of geometric shapes.

#### **Example:**

If $`A = \begin{bmatrix} 3 & 1 \\ 0 & 2 \end{bmatrix}`$, then:

$$
\det(A) = (3)(2) - (0)(1) = 6 \Rightarrow \text{Area Scale Factor} = |6| = \boxed{6}
$$

So, any area under this transformation is **multiplied by 6**.

---

### ✅ **Summary Table**

| Task                        | Method                                             |        | 
| --------------------------- |----------------------------------------------------|--------| 
| **Image of a point**        | Apply $`T(\mathbf{x}) = A\mathbf{x} + \mathbf{b}`$ |        |   
| **Image of a polygon**      | Transform all vertices and reconnect               |        |   
| **Orientation-preserving?** | Check sign of $`\det(A)`$                          |        |   
| **Area scaling**            | $`(\mid \det(A) \mid)`$                            |        |

---

### **Conclusion**

Understanding the **image of an affine transformation** is essential for visualizing geometric 
effects such as distortion, rotation, and scaling. By analyzing how the transformation acts 
on points, polygons, orientation, and area, we gain full control over its impact in applications 
ranging from graphics to robotics and machine learning.
