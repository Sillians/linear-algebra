## **The Dimension of the Null Space of a Matrix**

---

### **1. What Is the Null Space?**

The **null space** (or kernel) of a matrix $`A \in \mathbb{R}^{m \times n}`$ is the set of all solutions to the homogeneous equation:

$$
A\mathbf{x} = \mathbf{0}
$$

The **dimension** of the null space is called the **nullity** of $A$:

$$
\text{nullity}(A) = \dim(\text{Nul}(A))
$$

---

### **2. The Rank-Nullity Theorem**

For any $`A \in \mathbb{R}^{m \times n}`$:

$$
\text{rank}(A) + \text{nullity}(A) = n
$$

Where:

* $`\text{rank}(A)`$: Number of pivot columns
* $n$: Total number of columns
* $`\text{nullity}(A)`$: Number of free variables = number of non-pivot columns

---

### **3. Determining the Dimension of the Null Space Given the Number of Non-Pivot Columns**

After row-reducing the matrix:

* Count the **number of pivot columns** (basic variables).
* Subtract from the total number of columns to get the number of **free variables** (non-pivot columns), which equals the **nullity**.

#### Example:

A $`4 \times 6`$ matrix with 3 pivot columns:

$$
\text{nullity}(A) = 6 - 3 = 3
$$

This means the null space is a 3-dimensional subspace of $`\mathbb{R}^6`$.

---

### **4. Identifying the Dimension of the Null Space by Inspection**

Certain patterns reveal nullity quickly:

| Matrix Type                                     | Insight                                                  |
| ----------------------------------------------- | -------------------------------------------------------- |
| **Full Rank Square Matrix** (rank = n)          | Nullity = 0 (only solution is the zero vector)           |
| **More Columns than Rank**                      | Nullity = $`n - \text{rank}`$                              |
| **Zero Matrix** $`A \in \mathbb{R}^{m \times n}`$ | Nullity = $n$ (every vector satisfies $`A\mathbf{x} = 0`$) |

---

### **5. Finding the Nullity of a Matrix Using Row Reduction**

#### Procedure:

1. Row-reduce the matrix to its **REF** or **RREF**.
2. Identify the **pivot columns**.
3. Subtract the number of pivot columns from the total columns.

#### Example:

$$
A = \begin{bmatrix}
1 & 2 & 3 & 4 \\
0 & 1 & 2 & 3 \\
0 & 0 & 0 & 0 \\
\end{bmatrix}
$$

* Pivot columns: 1 and 2
* Total columns: 4

$$
\text{nullity}(A) = 4 - 2 = 2
$$

The solution set will have two free parameters, so the null space is a 2D subspace of $`\mathbb{R}^4`$.

---

### **6. Summary Table**

| Task                         | Method                                         | Result                             |
| ---------------------------- | ---------------------------------------------- | ---------------------------------- |
| Determine nullity via pivots | $`n - \text{pivot count}`$                       | Nullity = number of free variables |
| Inspect special matrices     | Apply patterns (e.g., full rank ⇒ nullity = 0) | Varies                             |
| Row-reduction                | RREF shows pivots and free variables           | Count free vars for nullity        |

---

### **7. Key Properties**

* The nullity measures how many **free directions** exist in the solution space.
* A higher nullity means more **degrees of freedom** in the homogeneous solution set.
* If $`\text{nullity}(A) = 0`$, then $`A\mathbf{x} = \mathbf{0}`$ has only the **trivial solution**.

---

### **8. Conceptual Insight**

The **null space** describes the set of inputs that are **annihilated** by the matrix. 
The **nullity** reflects how "non-invertible" or **degenerate** the transformation is in terms of losing information.
