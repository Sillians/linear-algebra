## **Indexed Sets**

An *indexed set* (or *indexed family of sets*) is a collection of sets labeled or "indexed"
by elements of another set, typically denoted by a subscript. This concept is foundational 
in set theory and analysis, particularly when dealing with sequences or infinite collections of sets.

---

### **Key Concepts**

#### **1. Identifying Elements of an Indexed Family**

An indexed family of sets is written as:

$$
\{A_i\}_{i \in I}
$$

* Here, $I$ is the *index set*, and each $`A_i`$ is a set corresponding to index $`i \in I`$.


* Example: Let $`I = \{1, 2, 3\}`$ and define $`A_i = \{i, i+1\}`$. Then:

$$
A_1 = \{1, 2\}, \quad A_2 = \{2, 3\}, \quad A_3 = \{3, 4\}
$$

#### **2. Finding Unions and Intersections of Finite Families of Indexed Sets**

For a finite index set $`I = \{1, 2, \dots, n\}`$:

* **Union**:

$$
\bigcup_{i=1}^n A_i = A_1 \cup A_2 \cup \dots \cup A_n
$$

* **Intersection**:

$$
\bigcap_{i=1}^n A_i = A_1 \cap A_2 \cap \dots \cap A_n
$$

Example:
Let $`A_1 = \{1, 2\}, A_2 = \{2, 3\}`$, then:

* $`\bigcup_{i=1}^2 A_i = \{1, 2, 3\}`$


* $`\bigcap_{i=1}^2 A_i = \{2\}`$

#### **3. Finding Unions and Intersections of (Countably) Infinite Families of Indexed Sets**

If $`I = \mathbb{N}`$, then the family is *countably infinite*.

Let:

$$
A_n = \{n, n+1, n+2, \dots\} = \{k \in \mathbb{N} : k \geq n\}
$$

* **Union**:

$$
\bigcup_{n=1}^{\infty} A_n = \mathbb{N}
$$

* **Intersection**:

$$
\bigcap_{n=1}^{\infty} A_n = \emptyset
$$

  (Because no natural number is in all $`A_n`$.)

---

### **Summary**

Indexed sets allow structured analysis of collections of sets. Understanding how to compute 
unions and intersections over both finite and infinite indexed families is essential for 
work in advanced mathematics, particularly in analysis, topology, and logic.
