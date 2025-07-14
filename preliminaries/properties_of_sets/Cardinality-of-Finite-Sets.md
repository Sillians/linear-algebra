## **Cardinality of Finite Sets**

The **cardinality** of a set is a measure of the **"number of elements"** in the set. 
For **finite sets**, this simply means **counting** how many distinct elements the set contains.

---

###  **1. Definition of Cardinality**

Let $A$ be a set. The **cardinality of $A$**, denoted $|A|$, is the **number of distinct elements** in the set.

#### ✅ Example:

$$
A = \{2, 4, 6\} \quad \Rightarrow \quad |A| = 3
$$

---

### **2. Important Properties of Cardinality**

* **Empty set**:

$$
|\emptyset| = 0
$$

* **Repeated elements** do **not** increase cardinality:

$$
B = \{1, 2, 2, 3\} \Rightarrow |B| = 3
$$

* **Subset property**:
  If $`A \subseteq B`$, then $`|A| \leq |B|`$

---

### **3. Operations and Cardinality**

#### ✅ **Union of Disjoint Sets**:

If $`A \cap B = \emptyset`$, then:

$$
|A \cup B| = |A| + |B|
$$

#### ✅ **General Union Formula**:

For any two sets:

$$
|A \cup B| = |A| + |B| - |A \cap B|
$$

#### ✅ **Cartesian Product**:

$$
|A \times B| = |A| \cdot |B|
$$

#### ✅ **Power Set**:

The power set of $A$, denoted $`\mathcal{P}(A)`$, has:

$$
|\mathcal{P}(A)| = 2^{|A|}
$$

---

### **4. Applications in Counting**

Cardinality helps in solving problems involving:

* **Combinatorics** (number of outcomes)


* **Probability** (defining sample spaces)


* **Logic and proof** (e.g., pigeonhole principle)

---

### **5. Examples**

#### Example 1:

$$
A = \{1, 2, 3\}, \quad B = \{3, 4, 5\}
$$

* $`|A| = 3`$, $`|B| = 3`$


* $`A \cap B = \{3\}`$


* $`|A \cup B| = 3 + 3 - 1 = 5`$

---

#### Example 2:

$$
C = \{a, b\}, \quad D = \{x, y, z\}
$$

* $`|C \times D| = 2 \cdot 3 = 6`$

---

### ✅ **Summary Table**

| Concept           | Formula                                                                      |                |       |   |       |   |   |          |   |
| ----------------- |------------------------------------------------------------------------------| -------------- | ----- | - | ----- | - | - | -------- | - |
| Cardinality       | $`( \mid A \mid )`$                                                          |   |       
| Empty set         | $`( \mid \emptyset \mid = 0 )`$                                              |   |    
| Union (general)   | $`( \mid A \cup B \mid = \mid A \mid + \mid0 B \mid - \mid A \cap B \mid )`$ |
| Cartesian product | $`( \mid A \times B  \mid = \mid A \mid \cdot \mid B  \mid )`$               |         
| Power set         | $`( \mid \mathcal{P}(A) \mid = 2^{ \mid A \mid } )`$                         |   |   

---

### **Conclusion**

The **cardinality of finite sets** is fundamental to set theory and combinatorics. 
It lays the groundwork for understanding **counting**, **probability**, and **set operations**, 
forming the basis for more advanced mathematical reasoning.
