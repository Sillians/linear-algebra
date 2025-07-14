## **The Dimension of a Span**

---

### **1. Understanding the Span and Its Dimension**

In linear algebra, the **span** of a set of vectors is the collection of all possible linear combinations of 
those vectors. The **dimension** of the span is the number of **linearly independent** vectors in the 
set—this tells you how many directions in space the span "reaches."

#### Definitions:

* **Span**:
  Given vectors $\mathbf{v}_1, \mathbf{v}_2, ..., \mathbf{v}_k \in \mathbb{R}^n$,
  the span is:

$`\text{Span}(\{\mathbf{v}_1, \mathbf{v}_2, ..., \mathbf{v}_k\}) = \left\{ \sum_{i=1}^{k} c_i \mathbf{v}_i \mid c_i \in \mathbb{R} \right\}`$

* **Dimension of the span** = Number of linearly independent vectors among $`\mathbf{v}_1, ..., \mathbf{v}_k`$

---

### **2. Finding the Dimension of a Span by Inspection**

When vectors are simple or obviously related, dimension can often be determined by observing relationships.

#### Examples:

1. If two vectors are scalar multiples:
   $`\mathbf{v}_1 = [1, 2], \mathbf{v}_2 = [2, 4]`$
   → Span is one-dimensional (they lie on the same line).

2. If no vector is a linear combination of the others:
   $`\mathbf{v}_1 = [1, 0], \mathbf{v}_2 = [0, 1]`$
   → Span is two-dimensional (full plane $`\mathbb{R}^2`$).

> **Tip**: Look for zero vectors, scalar multiples, or clear combinations.

---

### **3. Finding the Dimension of a Span Using Row Reduction**

When visual inspection is difficult (especially with more than 2 vectors), row reduction helps determine linear independence.

#### Steps:

1. **Form a matrix** $A$ where each vector is a column.


2. **Row reduce** the matrix (e.g., to row echelon or reduced row echelon form).


3. **Count the number of pivot columns**. This is the number of linearly independent columns and hence the **dimension of the span**.


#### Example:

Let

$$
A =
\begin{bmatrix}
1 & 2 & 3 \\
2 & 4 & 6
\end{bmatrix}
$$

Row reduce:

$$
\begin{bmatrix}
1 & 2 & 3 \\
0 & 0 & 0
\end{bmatrix}
\Rightarrow \text{Rank} = 1 \Rightarrow \dim(\text{Span}) = 1
$$

---

### **4. Summary Table**

| Situation                        | Span Dimension      | Method                      |
| -------------------------------- | ------------------- | --------------------------- |
| All vectors are scalar multiples | 1                   | Inspection or row reduction |
| Vectors are linearly independent | = number of vectors | Inspection or row reduction |
| Some linear dependence exists    | < number of vectors | Use row reduction           |

---

### **5. Geometric Interpretation**

* **Dimension 0**: Only the zero vector.
* **Dimension 1**: A line through the origin.
* **Dimension 2**: A plane through the origin.
* **Dimension n**: Full $`\mathbb{R}^n`$.

---

### **Key Insight**

The **dimension of the span** = **number of directions** the vectors can generate = **number of linearly independent vectors** = **rank** of the matrix formed by the vectors.

This concept is foundational in understanding vector spaces, subspaces, linear transformations, and rank-nullity.
