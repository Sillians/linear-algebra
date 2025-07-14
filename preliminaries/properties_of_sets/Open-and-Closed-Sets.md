# **Open and Closed Sets**

In topology and analysis, understanding **open** and **closed** sets helps define limits, continuity, and compactness. 
These concepts are foundational in $`\mathbb{R}`$, $`\mathbb{R}^2`$, and general metric or topological spaces.

---

##  **Definitions**

###  Open Set (in $`\mathbb{R}^n`$)

A set $`S`$ is **open** if for every point $`x \in S`$, there exists an $`\varepsilon > 0`$ such that the 
ball $`B\_\varepsilon(x) \subseteq S`$.

* In $`\mathbb{R}`$: An open interval $`(a, b)`$ is open.
* In $`\mathbb{R}^2`$: An open disk or region without boundary is open.

###  Closed Set (in $`\mathbb{R}^n`$)

A set $`S`$ is **closed** if it contains all its **limit points**, or equivalently, if its **complement** is open.

* In $`\mathbb{R}`$: A closed interval $`[a, b]`$ is closed.
* In $`\mathbb{R}^2`$: A region including its boundary.

---

## ✅ **Identifying Open and Closed Sets of Real Numbers**

| Set            | Open? | Closed? | Reason                              |
|----------------| ----- | ------- | ----------------------------------- |
| $`(1, 5)`$     | ✅     | ❌       | Open interval — no endpoints        |
| $`[2, 6]`$     | ❌     | ✅       | Includes endpoints                  |
| $`(0, 1]`$     | ❌     | ❌       | One endpoint missing — neither      |
| $`\mathbb{R}`$ | ✅     | ✅       | Both open and closed (clopen)       |
| $`\emptyset`$  | ✅     | ✅       | By convention, both open and closed |

---

## 🧮 **Identifying Open and Closed Sets in the Plane**

### 1. **Open Disk in $`\mathbb{R}^2`$**:

Let:

$$
D = \{ (x, y) \in \mathbb{R}^2 : x^2 + y^2 < 1 \}
$$

* ✅ Open
* ❌ Not closed
* No boundary points included

---

### 2. **Closed Disk in $`\mathbb{R}^2`$**:

Let:

$$
C = \{ (x, y) \in \mathbb{R}^2 : x^2 + y^2 \leq 1 \}
$$

* ❌ Not open
* ✅ Closed
* Contains all its limit points

---

### 3. **Annulus (neither)**:

Let:

$$
A = \{ (x, y) \in \mathbb{R}^2 : 1 \leq x^2 + y^2 < 4 \}
$$

* ❌ Not open (because of $`1 \leq`$)
* ❌ Not closed (because of $`<`$)
* ✅ Neither

---

## 🚫 **Identifying Sets That Are Neither Open Nor Closed**

Examples:

* **Half-open intervals**: $`(a, b]`$ or $`[a, b)`$
* **Mixed-boundary regions**: $`{ (x, y) \in \mathbb{R}^2 : x^2 + y^2 \leq 4, x > 0 }`$

Such sets include some but not all boundary points—violating definitions of both open and closed sets.

---

## **Summary Table**

| Set Type                    | Open | Closed | Example       |
| --------------------------- | ---- | ------ | ------------- |
| Open Interval               | ✅    | ❌      | $`(0, 1)`$    |
| Closed Interval             | ❌    | ✅      | $`[0, 1]`$    |
| Half-Open                   | ❌    | ❌      | $`(0, 1]`$     |
| Entire Space $`\mathbb{R}^n`$ | ✅    | ✅      | $`\mathbb{R}^2`$ |
| Empty Set $`\emptyset`$      | ✅    | ✅      | N/A           |

---