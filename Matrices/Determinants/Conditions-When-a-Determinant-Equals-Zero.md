## **Conditions When a Determinant Equals Zero**

The **determinant** of a square matrix reflects key geometric and algebraic properties: volume scaling, 
invertibility, and linear dependence. A determinant of **zero** indicates that the matrix 
is **singular**, **non-invertible**, and its rows/columns are **linearly dependent**.

---

### **1. Key Condition: When Is a Determinant Zero?**

A square matrix $A$ has $`\det(A) = 0`$ if and only if:

* Its rows or columns are **linearly dependent**
* The matrix is **not invertible**
* The matrix **collapses space** (e.g., flattens a 3D shape into 2D)
* The matrix has **no full rank**

---

### **2. Determinant with a Zero Row or Column**

If any **entire row or column is zero**, then:

$$
\boxed{\det(A) = 0}
$$

#### **Example:**

$$
A = \begin{bmatrix}
1 & 2 & 3 \\
0 & 0 & 0 \\
7 & 8 & 9
\end{bmatrix}
\Rightarrow \det(A) = 0
$$

Because one row is entirely zero, there is **no volume** in the transformed space.

---

### **3. Determinant with Two Identical Rows or Columns**

If two rows or columns in a matrix are **exactly the same**, then:

$$
\boxed{\det(A) = 0}
$$

Because identical vectors are linearly dependent.

#### **Example:**

$$
A = \begin{bmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
1 & 2 & 3
\end{bmatrix}
\Rightarrow \det(A) = 0
$$

Row 1 and Row 3 are identical → matrix is **singular**.

---

### **4. Determinant with Two Proportional Rows or Columns**

If one row or column is a **scalar multiple** of another, then:

$$
\boxed{\det(A) = 0}
$$

Because proportional rows/columns are also linearly dependent.

#### **Example:**

$$
A = \begin{bmatrix}
1 & 2 \\
3 & 6
\end{bmatrix}
\Rightarrow \text{Row 2} = 3 \cdot \text{Row 1} \Rightarrow \det(A) = 0
$$

---

### ✅ **Summary of Zero Determinant Conditions**

| Matrix Property                          | Result     |
| ---------------------------------------- | ---------- |
| One row or column is all zeros           | $\det = 0$ |
| Two rows or columns are identical        | $\det = 0$ |
| Two rows or columns are scalar multiples | $\det = 0$ |
| Rows/columns are linearly dependent      | $\det = 0$ |
| Matrix is singular (not invertible)      | $\det = 0$ |
| Rank of matrix < size                    | $\det = 0$ |

---

### **Geometric Insight**

* In 2D: determinant = **area** of the parallelogram spanned by row/column vectors.
* In 3D: determinant = **volume** of the parallelepiped.
* If rows/columns are dependent (e.g., lie on the same line or plane), the shape **collapses**, and **area/volume = 0**.

---

### **Conclusion**

Recognizing when a determinant equals zero is critical for understanding:

* **Linear dependence**
* **Matrix invertibility**
* **Solving systems of equations**
* **Geometric transformations**

It provides a powerful test for whether a matrix defines a meaningful transformation or collapses dimensions entirely.
