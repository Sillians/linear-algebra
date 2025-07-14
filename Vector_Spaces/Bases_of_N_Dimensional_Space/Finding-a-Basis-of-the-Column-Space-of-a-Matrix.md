## **Finding a Basis of the Column Space of a Matrix**

---

### **1. Overview**

The **column space** (or **range**) of a matrix $A \in \mathbb{R}^{m \times n}$, denoted $\text{Col}(A)$, is the subspace of $\mathbb{R}^m$ **spanned by the columns of $A$**.

A **basis** for the column space is a **linearly independent subset** of columns of $A$ that **span the column space**. Finding such a basis allows representation of any column of $A$ as a linear combination of the basis vectors.

---

### **2. Finding a Basis of the Column Space of a Matrix**

**Method: Use Gaussian Elimination (Row Reduction)**

**Steps**:

1. **Form the matrix $A$ and row-reduce it to echelon form (REF)** using elementary row operations.

2. **Identify pivot columns** in the REF—these correspond to the **linearly independent columns**.

3. The corresponding **columns in the original matrix $A$** (not the REF) form a basis for $\text{Col}(A)$.

#### **Example**:

Let

$$
A = \begin{bmatrix}
1 & 2 & 3 \\
2 & 4 & 6 \\
3 & 6 & 9
\end{bmatrix}
$$

1. Row-reduce:

$$
\text{REF}(A) = \begin{bmatrix}
1 & 2 & 3 \\
0 & 0 & 0 \\
0 & 0 & 0
\end{bmatrix}
$$

2. Pivot in column 1 → only column 1 is linearly independent.

3. **Basis**:

$`\left\{ \begin{bmatrix}1 \\ 2 \\ 3\end{bmatrix} \right\}`$

---

### **3. Determining Whether a Given Set Is a Basis of the Column Space of a Matrix With Two Rows**

Suppose $A \in \mathbb{R}^{2 \times n}$, and you're given a set of vectors $S = \{ \mathbf{v}_1, \dots, \mathbf{v}_k \} \subset \mathbb{R}^2$. To determine whether $S$ is a basis for $\text{Col}(A)$:

**Steps**:

1. **Compute the column space of $A$** by row-reducing as before.

2. Let $B = \{ \mathbf{c}_1, \dots, \mathbf{c}_r \}$ be a basis of $\text{Col}(A)$.

3. Check if $S$ is linearly independent.

4. Check if **every vector in $B$** can be written as a linear combination of vectors in $S$.

   * If both true ⇒ $S$ is a basis for $\text{Col}(A)$

#### **Example**:

Let

$`A = \begin{bmatrix} 1 & 2 & 3 \\0 & 1 & 1 \end{bmatrix}, \quad S = \left\{ \begin{bmatrix}1 \\ 0\end{bmatrix}, \begin{bmatrix}2 \\ 1\end{bmatrix} \right\}`$

Row-reducing $A$, the pivot columns are 1 and 2. So,

$`\text{Basis} = \left\{ \begin{bmatrix}1 \\ 0\end{bmatrix}, \begin{bmatrix}2 \\ 1\end{bmatrix} \right\}`$

Since $S$ exactly matches the basis, $S$ is indeed a basis for $`\text{Col}(A)`$.

---

### **4. Determining Whether a Given Set Is a Basis of the Column Space of a Matrix for a Larger Matrix**

Suppose $`A \in \mathbb{R}^{m \times n}`$ with $`m > 2`$. To verify if a given set $`S = \{ \mathbf{v}_1, \dots, \mathbf{v}_k \} \subset \mathbb{R}^m`$ is a basis of $`\text{Col}(A)`$:

**Steps**:

1. Find a basis $B$ for $`\text{Col}(A)`$ using Gaussian elimination or by computing the rank.

2. Check if:

   * $S$ is linearly independent (using rank or reduced row echelon form).
   * $`\text{span}(S) = \text{span}(B)`$, i.e., **same dimension and same span**.

3. Alternatively:

   * Stack $S$ as columns of matrix $M$
   * Stack $A$'s columns as matrix $N$
   * If $`\text{rank}(M) = \text{rank}(N)`$ and $`\text{col}(M) \subseteq \text{col}(N)`$, then $S$ is a basis.

#### **Example**:

Let

$`A = \begin{bmatrix} 1 & 0 & 2 & 3 \\2 & 0 & 4 & 6 \\3 & 0 & 6 & 9 \end{bmatrix}, \quad S = \left\{ \begin{bmatrix}1 \\ 2 \\ 3\end{bmatrix}, \begin{bmatrix}2 \\ 4 \\ 6\end{bmatrix} \right\}`$

Reduce $A$ → only column 1 is a pivot. Column 3 is a multiple of column 1. So:

* Basis of $`\text{Col}(A)`$ is:

$`\left\{ \begin{bmatrix}1 \\ 2 \\ 3\end{bmatrix} \right\}`$

* $S$ contains this vector and one dependent vector ⇒ Not linearly independent.

* So $S$ is **not a basis** of $`\text{Col}(A)`$.

---

### **Summary Table**

| **Task**                                    | **Steps**                                                                                                      |
| ------------------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| Find basis of column space                  | 1. Row reduce $A$ to REF <br> 2. Identify pivot columns <br> 3. Select corresponding columns from original $A$ |
| Check if set $S$ is a basis (small matrix)  | 1. Check span equals column space <br> 2. Check linear independence                                            |
| Check if set $S$ is a basis (larger matrix) | 1. Compare rank of $A$ and matrix with $S$'s columns <br> 2. Check span inclusion and independence             |

---
