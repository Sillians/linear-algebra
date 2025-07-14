## **Subsets**

A **subset** is a set that contains **only elements found in another set**. 
Understanding subsets is foundational in set theory, logic, combinatorics, and mathematical proofs.

---

### **1. Identifying Subsets of a Given Set**

A set $A$ is a **subset** of a set $B$ if **every element** of $A$ is also in $B$.
This is written as:

$$
A \subseteq B
$$

If $`A \subseteq B`$ and $`A \ne B`$, then $A$ is called a **proper subset**, denoted:

$$
A \subset B
$$

#### ✅ Example:

Let $`B = \{1, 2, 3\}`$, then:

* $`\{1\} \subseteq B`$
* $`\{1, 2\} \subseteq B`$
* $`\{1, 2, 3\} \subseteq B`$
* $`\{4\} \not\subseteq B`$

---

### **2. Finding All Subsets of a Given Set**

A set with $n$ elements has $`2^n`$ **subsets**, including:

* The **empty set** $`\emptyset`$
* The set itself

#### ✅ Example:

Let $`A = \{x, y\}`$

* Subsets:

$$
\emptyset,\ \{x\},\ \{y\},\ \{x, y\}
$$

* Total: $`2^2 = 4`$

For $`A = \{a, b, c\}`$, total subsets = $`2^3 = 8`$

---

### **3. Identifying Subsets of Special Sets**

Some commonly used sets and their subsets:

* $`\mathbb{N} \subset \mathbb{Z} \subset \mathbb{Q} \subset \mathbb{R} \subset \mathbb{C}`$
* Every set is a subset of itself.
* The empty set $`\emptyset`$ is a subset of **every set**.

#### ✅ Examples:

* $`\{2, 4\} \subseteq \{2, 4, 6, 8\}`$
* $`\emptyset \subseteq \mathbb{N}`$

---

### **4. Identifying True Statements About Subsets**

| Statement                      | True/False | Reason                                    |
| ------------------------------ | ---------- | ----------------------------------------- |
| $`\{1\} \subseteq \{1, 2\}`$     | ✅ True     | All elements of left set are in right set |
| $`\{1, 2\} \subset \{1, 2\}`$    | ❌ False    | They are equal, not a proper subset       |
| $`\emptyset \subseteq \{a, b\}`$ | ✅ True     | Empty set is subset of every set          |
| $`\{x, y\} \subset \{x, y, z\}`$ | ✅ True     | Proper subset                             |
| $`\{1, 2\} \subseteq \{3, 4\}`$  | ❌ False    | 1 and 2 not found in second set           |

---

### ✅ **Summary Table**

| Concept           | Description                                                  |
| ----------------- | ------------------------------------------------------------ |
| Subset            | $`A \subseteq B \iff \forall x (x \in A \Rightarrow x \in B)`$ |
| Proper subset     | $`A \subset B`$ and $`A \ne B`$                                  |
| Number of subsets | $`2^n`$, where $`n`$ is the number of elements                   |
| Empty set         | Subset of every set                                          |
| Every set         | Subset of itself                                             |

---

### **Conclusion**

Understanding subsets is key to reasoning about set relationships. Whether comparing data sets, 
structuring logic, or evaluating conditions in proofs or algorithms, subsets help define inclusion,
structure and hierarchy among collections of elements.
