# **Interiors and Boundaries of Sets**

---

## **1. Overview**

In topology and real analysis, understanding the **interior** and **boundary** of sets is crucial for:

* Characterizing open/closed sets
* Determining continuity and limits
* Analyzing the behavior of functions on domains

---

## **2. Definitions**

### **Interior of a Set**

Let $`S \subseteq \mathbb{R}^n`$. The **interior** of $`S`$, denoted by $`\text{int}(S)`$, is the set of all points in $`S`$ for which there exists an **open ball** entirely contained in $S$.

Formally:

$$
\text{int}(S) = \{ x \in S \mid \exists \epsilon > 0, B_\epsilon(x) \subseteq S \}
$$

Where:

$$
B_\epsilon(x) = \{ y \in \mathbb{R}^n \mid \|y - x\| < \epsilon \}
$$

---

### **Boundary of a Set**

The **boundary** of a set $S$, denoted by $`\partial S`$, consists of all points where **every open ball** around the point contains **both** points in $S$ and points **not in** $S$.

Formally:

$$
\partial S = \overline{S} \cap \overline{S^c}
$$

Where:

* $`\overline{S}`$ is the **closure** of $S$
* $`S^c`$ is the **complement** of $S$

---

## **3. Visual Intuition**

* The **interior** is the "core" of the set-points fully surrounded by the set.
* The **boundary** includes all “edge” points—touching both inside and outside the set.

---

## **4. Examples**

### **Example 1: Open Ball in $`\mathbb{R}^2`$**

Let $`S = B_1(0) = \{ x \in \mathbb{R}^2 \mid \|x\| < 1 \}`$

* $`\text{int}(S) = S`$ (all points are interior)
* $`\partial S = \{ x \in \mathbb{R}^2 \mid \|x\| = 1 \}`$ (the circle)

---

### **Example 2: Closed Interval $`[0, 1] \subseteq \mathbb{R}`$**

* $`\text{int}([0, 1]) = (0, 1)`$
* $`\partial [0, 1] = \{0, 1\}`$

---

### **Example 3: Rational Numbers $`\mathbb{Q} \subseteq \mathbb{R}`$**

* $`\text{int}(\mathbb{Q}) = \emptyset`$ (no open interval of rationals only)
* $`\partial \mathbb{Q} = \mathbb{R}`$

---

## **5. Identifying the Boundary of a Set**

To find $`\partial S`$:

1. Find the **closure** $`\overline{S}`$ — all points $`x`$ such that every open ball around $`x`$ intersects $`S`$
2. Find the closure of the **complement** $`\overline{S^c}`$
3. Intersect:

$$
\partial S = \overline{S} \cap \overline{S^c}
$$

---

## **6. Identifying the Interior of a Set**

To find $`\text{int}(S)`$:

* Look for all points in $`S`$ that lie inside some **open ball** completely contained in $`S`$.

---

## **7. Identifying True Statements Regarding Interiors and Boundaries**

Here are some **truth statements** that often appear in analysis:

| Statement                                               | Truth                                                    |
| ------------------------------------------------------- | -------------------------------------------------------- |
| $`\text{int}(S)`$ is always an open set                   | ✅ True                                                   |
| $`\partial S`$ is always a closed set                     | ✅ True                                                   |
| $`S = \text{int}(S) \cup \partial S`$ (if $S$ is closed)  | ✅ True                                                   |
| $`\text{int}(S) \cap \partial S = \emptyset`$             | ✅ True                                                   |
| $`\partial(S^c) = \partial S`$                            | ✅ True                                                   |
| $`\text{int}(S^c) = \mathbb{R}^n \setminus \overline{S}`$ | ❌ False (correct: $`\mathbb{R}^n \setminus \text{cl}(S)`$) |
| $`\partial(\text{int}(S)) \subseteq \partial(S)`$         | ✅ True                                                   |

---

## Summary Table

| **Concept** | **Definition**                                                                       |
| ----------- | ------------------------------------------------------------------------------------ |
| Interior    | $`\text{int}(S) = \{ x \in S \mid \exists \epsilon > 0, B_\epsilon(x) \subseteq S \}`$ |
| Boundary    | $`\partial S = \overline{S} \cap \overline{S^c}`$                                     |
| Closure     | All limit points of $`S`$ plus all points in $`S`$                                       |
| Open Set    | A set that equals its own interior                                                   |
| Closed Set  | A set that contains its boundary                                                     |

---
