## **Describing Planar Regions Using Set-Builder Notation**

---

### **1. Set-Builder Notation Overview**

Set-builder notation is a concise way to define a set by stating the **properties** its members must satisfy. 
In the plane $`\mathbb{R}^2`$, a planar region is a subset of points $`(x, y) \in \mathbb{R}^2`$ satisfying one or more inequalities.

General form:

$$
\{ (x, y) \in \mathbb{R}^2 : \text{condition(s) on } x \text{ and } y \}
$$

---

### **2. Describing Rectangular Sets Using Set-Builder Notation**

A **rectangular region** is bounded by horizontal and vertical lines. Suppose we have a rectangle defined by:

* Horizontal bounds: $`a \leq x \leq b`$


* Vertical bounds: $`c \leq y \leq d`$


Then the set-builder notation is:

$$
\{ (x, y) \in \mathbb{R}^2 : a \leq x \leq b, \ c \leq y \leq d \}
$$

**Example:**
A rectangle with corners at (1, 2) and (4, 5):

$$
\{ (x, y) \in \mathbb{R}^2 : 1 \leq x \leq 4, \ 2 \leq y \leq 5 \}
$$

---

### **3. Linear Boundaries – One Condition**

A single **linear inequality** describes a **half-plane**. A linear equation has the form $`ax + by = c`$. 
The half-plane is defined by:


* $`ax + by \leq c`$ (region **on or below** the line)


* $`ax + by \geq c`$ (region **on or above** the line)

**Example:**
The region **below** the line $`y = 2x + 1`$:

$$
\{ (x, y) \in \mathbb{R}^2 : y \leq 2x + 1 \}
$$

---

### **4. Linear Boundaries – Two Conditions**

If two linear inequalities are used, they define a **strip** or **bounded polygonal region**.

**Example:**
The region **between** the lines $`y = x`$ and $`y = 2x + 1`$:

$$
\{ (x, y) \in \mathbb{R}^2 : x \leq y \leq 2x + 1 \}
$$


**Example:**
The region **between** two vertical lines $`x = 1`$ and $`x = 3`$, and **below** the line $`y = 5`$:

$$
\{ (x, y) \in \mathbb{R}^2 : 1 \leq x \leq 3, \ y \leq 5 \}
$$

---

### **5. Describing Non-Rectangular Sets Using Set-Builder Notation**

Non-rectangular regions include curved boundaries (like circles, parabolas, ellipses) or combinations of lines and curves.

#### **(a) Parabolic Region**

**Shaded area between parabola $`y = x^2`$ and line $`y = 4`$:**

$$
\{ (x, y) \in \mathbb{R}^2 : x^2 \leq y \leq 4 \}
$$

This includes all points lying **above** the parabola and **below** the line $`y = 4`$.


#### **(b) Circular Disk**

A circle with radius $r$ centered at the origin:

* **Interior (open disk):** $`x^2 + y^2 < r^2`$


* **Closed disk:** $`x^2 + y^2 \leq r^2`$

Set-builder notation:

$$
\{ (x, y) \in \mathbb{R}^2 : x^2 + y^2 \leq r^2 \}
$$


#### **(c) Elliptical Region**

Ellipse centered at origin with semi-axes $a$, $b$:

$$
\{ (x, y) \in \mathbb{R}^2 : \frac{x^2}{a^2} + \frac{y^2}{b^2} \leq 1 \}
$$

---

### **6. Intersections and Unions in Set-Builder Notation**

* **Intersection** (AND): Use a comma to combine conditions:

$$
\{ (x, y) \in \mathbb{R}^2 : 0 \leq x \leq 2, \ y \leq x + 1 \}
$$

* **Union** (OR): Use a union symbol or logical “or”:

$$
\{ (x, y) \in \mathbb{R}^2 : y \leq x^2 \} \cup \{ (x, y) \in \mathbb{R}^2 : y \geq 4 \}
$$

---

### **Summary**

| **Type**          | **Example**                            | **Set-Builder Notation**                                               |
| ----------------- | -------------------------------------- | ---------------------------------------------------------------------- |
| Rectangle         | $`1 \leq x \leq 3, 2 \leq y \leq 5`$     | $`\{ (x, y) \in \mathbb{R}^2 : 1 \leq x \leq 3, 2 \leq y \leq 5 \}`$     |
| Half-Plane        | Below line $`y = x`$                     | $`\{ (x, y) \in \mathbb{R}^2 : y \leq x \}`$                             |
| Between two lines | Between $`y = x`$ and $`y = 2x`$           | $`\{ (x, y) \in \mathbb{R}^2 : x \leq y \leq 2x \}`$                     |
| Parabolic strip   | Between $`y = x^2`$ and $`y = 4`$          | $`\{ (x, y) \in \mathbb{R}^2 : x^2 \leq y \leq 4 \}`$                    |
| Disk              | Inside circle $`x^2 + y^2 \leq 9`$       | $`\{ (x, y) \in \mathbb{R}^2 : x^2 + y^2 \leq 9 \}`$                     |
| Ellipse           | $`\frac{x^2}{9} + \frac{y^2}{4} \leq 1`$ | $`\{ (x, y) \in \mathbb{R}^2 : \frac{x^2}{9} + \frac{y^2}{4} \leq 1 \}`$ |

---

This foundation allows structured and precise descriptions of any planar region, linear or curved, bounded or unbounded, rectangular or irregular.
