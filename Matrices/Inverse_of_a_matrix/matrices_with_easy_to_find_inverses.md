## **Matrices with Easy-to-Find Inverses**

In general, finding the inverse of an $`n \times n`$ matrix can be computationally intensive. 
However, certain special types of matrices have inverses that are **fast and straightforward 
to compute** due to their structure. Three important types are:

* **Diagonal matrices**
* **Permutation matrices**
* **Frobenius matrices**

---

### **1. Inverting a Diagonal Matrix**

A **diagonal matrix** is a square matrix where all entries **outside the main diagonal are zero**:

$$
D = \begin{bmatrix}
d_1 & 0 & \cdots & 0 \\
0 & d_2 & \cdots & 0 \\
\vdots & \vdots & \ddots & \vdots \\
0 & 0 & \cdots & d_n
\end{bmatrix}
$$

**Inverse Rule:**

If **none** of the diagonal entries are zero ($`d_i \ne 0`$ for all $`i`$), then the inverse is simply:

$$
D^{-1} = \begin{bmatrix}
\frac{1}{d_1} & 0 & \cdots & 0 \\
0 & \frac{1}{d_2} & \cdots & 0 \\
\vdots & \vdots & \ddots & \vdots \\
0 & 0 & \cdots & \frac{1}{d_n}
\end{bmatrix}
$$

**Why easy**: Only invert scalars; no row operations needed.

---

### **2. Inverting a Permutation Matrix**

A **permutation matrix** is a square matrix obtained by **rearranging the rows** of the identity matrix. 
Each row and column has exactly **one entry of 1**, and all others are 0.

Example:

$$
P = \begin{bmatrix}
0 & 1 & 0 \\
1 & 0 & 0 \\
0 & 0 & 1
\end{bmatrix}
$$

This swaps rows 1 and 2.

**Inverse Rule:**

The inverse of a permutation matrix is its **transpose**:

$$
P^{-1} = P^T
$$

**Why easy**: Permutations are orthogonal; row swaps are reversed by column swaps.

---

### **3. Inverting a Frobenius Matrix**

A **Frobenius matrix** (also called an **elementary lower triangular matrix**) is of the form:

$$
F = I + \alpha \cdot \mathbf{u} \mathbf{v}^T
$$

But more commonly for Gaussian elimination steps, it has a form like:

$$
F = \begin{bmatrix}
1 & 0 & 0 & 0 \\
l_{21} & 1 & 0 & 0 \\
l_{31} & 0 & 1 & 0 \\
l_{41} & 0 & 0 & 1 \\
\end{bmatrix}
$$

It performs a **row operation**: subtracting multiples of row 1 from lower rows.

**Inverse Rule:**

Negate the off-diagonal entries in the first column:

$` F^{-1} = \begin{bmatrix}  1 & 0 & 0 & 0 \\ - l_{21} & 1 & 0 & 0 \\ - l_{31} & 0 & 1 & 0 \\ - l_{41} & 0 & 0 & 1  \end{bmatrix} `$

**Why easy**: Reflects the reverse of the row operation. Only a few entries change.

---

### **4. Summary Table**

| Matrix Type        | Inversion Method           | Condition                   |
| ------------------ | -------------------------- | --------------------------- |
| Diagonal Matrix    | Invert each diagonal entry | All $d_i \ne 0$             |
| Permutation Matrix | Transpose of the matrix    | Always invertible           |
| Frobenius Matrix   | Negate row-op coefficients | Corresponds to valid row op |

---

These matrix types frequently arise in **LU decomposition**, **row operations**, and **efficient 
computation**, making them extremely useful in numerical linear algebra and optimization.
