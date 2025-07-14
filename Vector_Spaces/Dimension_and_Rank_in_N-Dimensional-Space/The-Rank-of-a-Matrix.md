## **The Rank of a Matrix**

---

### **1. What Is the Rank of a Matrix?**

The **rank** of a matrix is the dimension of its **column space**, i.e., the number of linearly independent columns. 
Equivalently, it is the number of **pivot columns** in its **row echelon form (REF)** or **reduced row echelon form (RREF)**.

If $`A \in \mathbb{R}^{m \times n}`$, then:

$$
\text{rank}(A) = \dim(\text{Col}(A)) = \text{number of pivot columns}
$$

---

### **2. Determining the Rank of a Matrix Given the Number of Pivot Columns**

In any row-echelon form of a matrix:

* **Pivot columns** are those that contain the leading (non-zero) entries in each row.
* Each pivot corresponds to a linearly independent column in the original matrix.

#### Example:

If a $`4 \times 5`$ matrix has 3 pivot columns, then:

$$
\text{rank}(A) = 3
$$

This means its column space is a 3-dimensional subspace of $`\mathbb{R}^4`$.

---

### **3. Identifying the Matrix With a Given Rank by Inspection**

Some cases where the rank can be determined without computation:

| Matrix Type                                  | Rank Insight                                     |
| -------------------------------------------- | ------------------------------------------------ |
| **Zero Matrix**                              | Rank = 0                                         |
| **Identity Matrix $`I_n`$**                    | Rank = $`n`$, all columns are linearly independent |
| **Matrix with Repeated Columns**             | Rank < number of columns                         |
| **Upper/Lower Triangular with no zero rows** | Rank = number of nonzero rows or pivot positions |

#### Example:

$$
A = \begin{bmatrix}
1 & 2 & 3 \\
0 & 0 & 0 \\
0 & 1 & 2 \\
\end{bmatrix}
\Rightarrow \text{rank}(A) = 2
$$

(two pivot positions: column 1 and column 3 after row reduction)

---

### **4. Finding the Rank of a Matrix Using Row Reduction**

#### Procedure:

1. Apply **Gaussian elimination** to bring the matrix into **REF** or **RREF**.
2. Count the number of **nonzero rows** (equivalently, pivot positions).
3. This count is the **rank**.

#### Example:

Given:

$$
A = \begin{bmatrix}
1 & 2 & 3 \\
2 & 4 & 6 \\
1 & 1 & 1
\end{bmatrix}
$$

Row reduce:

* $`R_2 \leftarrow R_2 - 2R_1`$
* $`R_3 \leftarrow R_3 - R_1`$

$$
\Rightarrow \begin{bmatrix}
1 & 2 & 3 \\
0 & 0 & 0 \\
0 & -1 & -2
\end{bmatrix}
\Rightarrow \text{rank}(A) = 2
$$

---

### **5. Summary Table**

| Task                               | Method                                             | Result                        |
| ---------------------------------- | -------------------------------------------------- | ----------------------------- |
| Find rank using pivot columns      | Count pivot positions in REF/RREF                  | Rank = number of pivots       |
| Identify matrix rank by inspection | Use known forms (e.g., identity, zero, duplicates) | Varies                        |
| Find rank using row reduction      | Gaussian or Gauss-Jordan elimination               | Rank = number of nonzero rows |

---

### **6. Key Properties of Rank**

* $`\text{rank}(A) \leq \min(m, n)`$ for $`A \in \mathbb{R}^{m \times n}`$
* $`\text{rank}(A) = \text{rank}(A^T)`$
* Rank is preserved under **row operations** but not necessarily under **column operations**.

---

### **7. Conceptual Insight**

The **rank** of a matrix tells:

* How many **linearly independent vectors** are in its columns.
* The **dimension of the image** of the linear transformation represented by the matrix.
* How “invertible” or “non-degenerate” the matrix is in terms of data compression and solving linear systems.
