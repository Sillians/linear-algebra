## **Subspaces of N-Dimensional Space: Geometric Interpretation**

---

### **1. Definition of a Subspace in N-Dimensional Space**

A **subspace** of $`\mathbb{R}^n`$ is a subset $`V \subseteq \mathbb{R}^n`$ that satisfies three key properties:

1. **Contains the zero vector**: $`\vec{0} \in V`$


2. **Closed under vector addition**: If $`\vec{u}, \vec{v} \in V`$, then $`\vec{u} + \vec{v} \in V`$


3. **Closed under scalar multiplication**: If $`\vec{v} \in V`$, and $`c \in \mathbb{R}`$, then $`c\vec{v} \in V`$

Geometrically, subspaces are flat, infinite, and pass through the origin (e.g., lines or planes in $`\mathbb{R}^2`$, $`\mathbb{R}^3`$).

---

### **2. Identifying Whether Sets Represented Graphically Are Subspaces in Two-Dimensional Space**

In $`\mathbb{R}^2`$:

* **Lines through the origin** are subspaces.
  Example: Line defined by $`y = 2x`$ or $`y = -x`$


* **Lines not through the origin** are not subspaces.
  Example: $`y = x + 1`$ violates the zero vector condition.


* **The entire $`\mathbb{R}^2`$** is a subspace of itself.


* **Regions (like circles or bounded areas)** are **not** subspaces due to a lack of closure and/or missing the origin.

✔️ **Check**:

* Is the origin included?


* Is the structure flat and infinitely extending?

---

### **3. Identifying Whether Sets Represented Graphically Are Subspaces in Three-Dimensional Space**

In $`\mathbb{R}^3`$:

* **Lines and planes through the origin** are subspaces.
  Examples:

  * Line: $`\vec{v} = t \begin{bmatrix} 1 \\ 0 \\ 2 \end{bmatrix}`$
  * Plane: $`x + y + z = 0`$


* **Planes not passing through the origin** are not subspaces.
  Example: $`x + y + z = 1`$



* **Curved surfaces (e.g., spheres, cones)** are **not** subspaces.


* **The whole $`\mathbb{R}^3`$** is a subspace of itself.


✔️ **Check**:

* Does the plane or line pass through the origin?


* Is it flat (not curved or bounded)?


* Is it closed under vector addition and scalar multiplication?

---

### **4. Identifying Whether Sets Represented Using Set Notation Are Subspaces**

For a set defined as:

$$
S = \{ \vec{x} \in \mathbb{R}^n : \text{some condition on } \vec{x} \}
$$

Apply the **three tests**:

#### **(i) Contains the zero vector**:

Test if $`\vec{0}`$ satisfies the condition.

#### **(ii) Closed under addition**:

Test if $`\vec{u}, \vec{v} \in S \Rightarrow \vec{u} + \vec{v} \in S`$

#### **(iii) Closed under scalar multiplication**:

Test if $`\vec{u} \in S \Rightarrow c \vec{u} \in S`$ for all scalars $`c \in \mathbb{R}`$

---

### **Examples Using Set Notation**

* **Valid Subspace**:

$`V = \left\{ \begin{bmatrix} x \\ y \end{bmatrix} \in \mathbb{R}^2 : 3x - 2y = 0 \right\}`$

  A line through the origin → satisfies all 3 properties.

* **Invalid Subspace**:

$`V = \left\{ \begin{bmatrix} x \\ y \end{bmatrix} \in \mathbb{R}^2 : x^2 + y^2 = 1 \right\}`$

  Circle of radius 1 → not closed under addition or scalar multiplication.

---

### **Key Takeaways**

| Property                    | Required for Subspace? |
| --------------------------- | ---------------------- |
| Includes the origin         | ✔️                     |
| Closed under addition       | ✔️                     |
| Closed under multiplication | ✔️                     |
| Bounded or curved shape     | ❌                      |
| Finite set of points        | ❌                      |
| Passes through origin only  | ✔️                     |

Subspaces are **geometrically flat**, **algebraically linear**, and **infinite**.
