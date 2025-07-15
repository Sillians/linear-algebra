## **Row Operations on 2×2 Matrices as Products of Elementary Matrices**

---

### **1. What Are Elementary Matrices?**

An **elementary matrix** is a matrix obtained by performing **a single row operation** on an identity matrix. These matrices, 
when **left-multiplied** to another matrix, **perform that row operation** on the matrix.

There are **three types of elementary row operations**:

1. **Row swap**: $`R_i \leftrightarrow R_j`$
2. **Row scaling**: $`R_i \to k R_i`$ where $`k \ne 0`$
3. **Row replacement**: $`R_i \to R_i + k R_j`$

---

### **2. Elementary Matrices for 2×2 Matrices**

Given a 2×2 identity matrix $I = \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix}$:

| Operation                        | Elementary Matrix                                    |
|----------------------------------|------------------------------------------------------|
| Swap $`R_1 \leftrightarrow R_2`$ | $`E = \begin{bmatrix} 0 & 1 \\ 1 & 0 \end{bmatrix}`$ |
| Multiply $`R_1 \to k R_1`$       | $`E = \begin{bmatrix} k & 0 \\ 0 & 1 \end{bmatrix}`$ |
| Multiply $`R_2 \to k R_2`$       | $`E = \begin{bmatrix} 1 & 0 \\ 0 & k \end{bmatrix}`$ |
| Add $`k R_2`$ to $`R_1`$         | $`E = \begin{bmatrix} 1 & k \\ 0 & 1 \end{bmatrix}`$ |
| Add $`k R_1`$ to $`R_2`$         | $`E = \begin{bmatrix} 1 & 0 \\ k & 1 \end{bmatrix}`$ |

---

### **3. Left Multiplication Applies the Operation**

For a 2×2 matrix $A$, applying a row operation using an elementary matrix $E$ is done by:

$$
E A
$$

---

### **4. Example: Finding a Row Operation Equivalent to Left Multiplication**

#### Example:

Let $`E = \begin{bmatrix} 1 & 3 \\ 0 & 1 \end{bmatrix}`$

This is the identity matrix with **3 times Row 2 added to Row 1**, so:

* Operation: $`R_1 \to R_1 + 3R_2`$

#### Verify:

Let $`A = \begin{bmatrix} a & b \\ c & d \end{bmatrix}`$

Then:

$`EA = \begin{bmatrix} 1 & 3 \\ 0 & 1 \end{bmatrix} \begin{bmatrix} a & b \\ c & d \end{bmatrix} = \begin{bmatrix} a + 3c & b + 3d \\ c & d \end{bmatrix}`$

Which matches $`R_1 \to R_1 + 3R_2`$

---

### **5. Example: Matrix Product Equivalent to a Given Row Operation**

Suppose the row operation is:
**Multiply Row 2 by 4**, i.e., $`R_2 \to 4R_2`$

Then the elementary matrix is:

$`E = \begin{bmatrix} 1 & 0 \\ 0 & 4 \end{bmatrix}`$

If $A$ is any 2×2 matrix, then $EA$ applies the row scaling to $`R_2`$.

---

### **6. Matrix Product for a Sequence of Row Operations**

Suppose we perform the following on a matrix $A$:

1. $`R_2 \to R_2 + 2R_1`$
2. $`R_1 \leftrightarrow R_2`$

Corresponding elementary matrices:

* Step 1: $`E_1 = \begin{bmatrix} 1 & 0 \\ 2 & 1 \end{bmatrix}`$


* Step 2: $`E_2 = \begin{bmatrix} 0 & 1 \\ 1 & 0 \end{bmatrix}`$

Then the full transformation is:

$$
E_2 E_1 A
$$

That is: apply $`E_1`$ to $A$, then apply $`E_2`$ to the result.

---

### **7. Key Takeaways**

| Concept                        | Summary                                                                       |
| ------------------------------ | ----------------------------------------------------------------------------- |
| **Elementary Matrix**          | Matrix representing a single row operation                                    |
| **Left Multiplication**        | Applies the row operation to the matrix                                       |
| **Sequence of Row Operations** | Represented as a **product of elementary matrices**                           |
| **Reversibility**              | Every elementary matrix is **invertible**, and its inverse is also elementary |

---

### Summary

* **Each row operation** on a 2×2 matrix corresponds to an **elementary matrix**.



* Left-multiplying a matrix by that elementary matrix performs the row operation.



* **Multiple operations** = product of the corresponding elementary matrices.


* This concept is essential in matrix inversion, LU decomposition, and Gaussian elimination.
