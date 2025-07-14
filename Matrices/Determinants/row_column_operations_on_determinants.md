## **Row and Column Operations on Determinants**

Determinants are sensitive to elementary row and column operations. Understanding how these 
operations affect the determinant is key to efficient computation, especially during Gaussian elimination or LU decomposition.

---

### **1. Effect of Elementary Row or Column Operations on Determinants**

| Operation                                       | Effect on Determinant          |
| ----------------------------------------------- | ------------------------------ |
| **Swap two rows or columns**                    | Multiplies determinant by $-1$ |
| **Multiply a row or column by $k$**             | Multiplies determinant by $k$  |
| **Add a multiple of one row/column to another** | No effect on determinant       |

---

### **2. Calculating a Determinant After Switching Two Rows**

If you **interchange** two rows (or columns) of a matrix, the **sign of the determinant changes**:

$$
\det(B) = -\det(A)
$$

**Example:**

Let

$$
A = \begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix}, \quad \det(A) = (1)(4) - (2)(3) = -2
$$

Swapping rows:

$$
B = \begin{bmatrix} 3 & 4 \\ 1 & 2 \end{bmatrix}, \quad \det(B) = (3)(2) - (4)(1) = 6 - 4 = 2 = -(-2)
$$

---

### **3. Calculating a Determinant After Multiplying a Row by a Number**

If you multiply **one row or column** of a matrix by a scalar $k$, the **determinant is multiplied by $k$**:

$$
\det(B) = k \cdot \det(A)
$$

If **multiple rows** are scaled, the determinant is multiplied by the **product of the scalars**.

---

### **4. Calculating a Determinant After Multiplying the Entire Matrix by a Scalar**

If every entry of an $n \times n$ matrix is multiplied by a scalar $k$, the determinant is multiplied by $k^n$:

$$
\det(kA) = k^n \cdot \det(A)
$$

**Why?** Each row scaling multiplies the determinant by $k$, and there are $n$ rows.

---

### **5. Calculating a Determinant After Applying Several Elementary Row Operations**

Let’s analyze the effect cumulatively:

* **Row swap** → Multiply determinant by $-1$


* **Row scaling by $k$** → Multiply determinant by $k$


* **Row replacement (e.g., $`R_i \to R_i + mR_j`$)** → No change to determinant

**Example:**

Let

$$
A = \begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix}, \quad \det(A) = -2
$$

1. Multiply Row 1 by 3:

$$
\Rightarrow \det = 3 \cdot (-2) = -6
$$

2. Swap rows:

$$
\Rightarrow \det = -(-6) = 6
$$

3. Add 5×Row 1 to Row 2:

$$
\Rightarrow \det = 6 \ (\text{unchanged})
$$

---

### **6. Summary**

| Operation                            | Determinant Effect                             |
| ------------------------------------ |------------------------------------------------|
| Swap rows/columns                    | Multiply by $-1$                               |
| Scale a row/column by $k$            | Multiply by $k$                                |
| Add a multiple of one row to another | No change                                      |
| Multiply entire matrix by $k$        | Multiply by $k^n$ for an $`n \times n`$ matrix |

Understanding these rules allows you to simplify determinants using row operations while keeping track of how each operation modifies the result. This is especially useful when reducing matrices to upper triangular form, where the determinant is the **product of the diagonal entries** (after accounting for operation effects).
