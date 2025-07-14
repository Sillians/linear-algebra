## **Interior and Boundary Points**

---

### **1. Key Definitions**

* **Interior Point:** A point $`x \in A`$ is called an **interior point** of a set $`A \subseteq \mathbb{R}^n`$ if there exists an open ball centered at $x$ entirely contained in $A$. In symbols:
  $`x \in A \text{ is interior } \iff \exists \varepsilon > 0 \text{ such that } B(x, \varepsilon) \subseteq A`$


* **Boundary Point:** A point $`x \in \mathbb{R}^n`$ is a **boundary point** of $A$ if every open ball around $x$ contains at least one point in $A$ and at least one point not in $A$. In symbols:
  $`x \in \partial A \iff \forall \varepsilon > 0, B(x, \varepsilon) \cap A \neq \emptyset \text{ and } B(x, \varepsilon) \cap A^c \neq \emptyset`$


* **Closure:** The closure of a set $A$, denoted $`\overline{A}`$, includes all its interior and boundary points.


* **Open Set:** A set is open if all of its points are interior points.


* **Closed Set:** A set is closed if it contains all its boundary points.

---

### **2. Identifying Interior and Boundary Points of Sets of Real Numbers**

For sets in $`\mathbb{R}`$:

* Example: Let $`A = (1, 5)`$. Then:

  * Interior points: All $`x \in (1, 5)`$
  * Boundary points: $`x = 1`$ and $`x = 5`$
  * $`A`$ is open; $`\overline{A} = [1, 5]`$

* Example: Let $`B = [2, 4)`$. Then:

  * Interior points: All $`x \in (2, 4)`$
  * Boundary points: $`x = 2`$ and $`x = 4`$
  * $B$ is neither open nor closed

---

### **3. Identifying True Statements From a Diagram**

For visual regions in $`\mathbb{R}^2`$, pay attention to:

* **Shaded Area:** Usually represents the set.
* **Boundary Line/Dot:** Solid indicates inclusion ($`\leq, \geq`$); dashed indicates exclusion ($`<, >`$).
* **Interior:** All points where a small open ball lies entirely within the region.
* **Boundary:** Points on the edge of the region.

---

### **4. Interior and Boundary Points From Linear Inequalities**

Example: $`A = \{ (x, y) \in \mathbb{R}^2 : x + y < 1 \}`$

* **Interior:** All $`(x, y)`$ such that $`x + y < 1`$
* **Boundary:** The line $`x + y = 1`$
* $A$ is open (no boundary points included)

Example: $`B = \{ (x, y) : x + y \leq 1 \}`$

* Boundary: Again $`x + y = 1`$
* This time $`B`$ is closed (contains boundary)
* Interior: $`x + y < 1`$

---

### **5. Interior and Boundary Points From Nonlinear Inequalities**

Example: $`C = \{ (x, y) : x^2 + y^2 > 1 \}`$

* Interior: Region strictly outside the unit circle
* Boundary: Circle $`x^2 + y^2 = 1`$
* $C$ is open

Example: $`D = \{ (x, y) : x^2 + y^2 \geq 1 \}`$

* Interior: Same as above
* Boundary included
* $D$ is closed

---

### **Summary**

| Type            | Interior Points   | Boundary Points   |
| --------------- | ----------------- | ----------------- |
| Open Interval   | $`(a, b)`$          | $`a, b`$            |
| Closed Disk     | $`x^2 + y^2 < r^2`$ | $`x^2 + y^2 = r^2`$ |
| Linear Region   | $`x + y < 1`$       | $`x + y = 1`$       |
| Nonlinear Curve | $`x^2 + y^2 > 1`$   | $`x^2 + y^2 = 1`$   |

A systematic approach involves checking if a point is in the set, and whether a ball around it includes only points 
from within or from both inside and outside the set.
