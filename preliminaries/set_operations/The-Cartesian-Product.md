## **The Cartesian Product**

---

### **1. What is a Cartesian Product?**

The **Cartesian product** of two sets $`A`$ and $`B`$, denoted $`A \times B`$, is the set of **all ordered pairs** where 
the first element is from $`A`$ and the second is from $`B`$.

$$
A \times B = \{ (a, b) \mid a \in A,\, b \in B \}
$$

---

### **2. Creating a Schematic for a Cartesian Product**

To **visualize** a Cartesian product:

* List all elements of $`A`$ along one axis (horizontal).


* List all elements of $`B`$ along the other axis (vertical).


* Draw lines or grid points where combinations occur.

**Example:**

Let $`A = \{1, 2\}`$, $`B = \{x, y\}`$

Schematic:

```
       x       y
1 →   (1,x)  (1,y)  
2 →   (2,x)  (2,y)
```

Each grid point represents a unique ordered pair in $`A \times B`$.

---

### **3. Computing a Cartesian Product**

Let $`A = \{1, 2\}`$, $`B = \{x, y\}`$

Then:

$$
A \times B = \{ (1,x), (1,y), (2,x), (2,y) \}
$$

Note:

* **Order matters**: $`(1, x) \neq (x, 1)`$


* $`A \times B \neq B \times A`$ unless $`A = B`$ and elements are symmetrically paired

---

### **4. Computing the Cardinality of a Cartesian Product**

If $`|A| = m`$ and $`|B| = n`$, then:

$$
|A \times B| = m \cdot n
$$

**Example:**
If $`A = \{1, 2, 3\}`$, $`B = \{x, y\}`$, then:

$$
|A \times B| = 3 \cdot 2 = 6
$$

---

### **5. Cartesian Products With Three Sets**

For sets $A$, $B$, and $C$:

$$
A \times B \times C = \{ (a, b, c) \mid a \in A,\, b \in B,\, c \in C \}
$$

**Example:**
Let $`A = \{1\}`$, $`B = \{x, y\}`$, $`C = \{α, β\}`$

$$
A \times B \times C = \{ (1, x, α), (1, x, β), (1, y, α), (1, y, β) \}
$$

**Cardinality:**

$$
|A \times B \times C| = |A| \cdot |B| \cdot |C|
$$

---

### ✅ **Summary**

| Concept       | Description                                    |            |   |   |       |   |   |
| ------------- | ---------------------------------------------- | ---------- | - | - | ----- | - | - |
| $`A \times B`$  | All ordered pairs from $`A`$ and $`B`$             |            |   |   |       |   |   |
| Visualization | Grid or table of pairings                      |            |   |   |       |   |   |
| Cardinality   | Product of set sizes: (                        | A \times B | = | A | \cdot | B | ) |
| 3-Set Product | Tuples of form $`(a, b, c)`$, extended similarly |            |   |   |       |   |   |

The Cartesian product is a foundation in set theory, logic, coordinate systems, and database operations.
