## **Elementary 3×3 Matrices**

---

### **1. What is an Elementary Matrix?**

An **elementary matrix** is obtained by performing a **single elementary row operation** on an identity matrix.

For 3×3 matrices, there are three types:

* **Type I**: Row switching
* **Type II**: Row multiplication by a nonzero scalar
* **Type III**: Adding a multiple of one row to another

Let \$I\_3\$ denote the \$3 \times 3\$ identity matrix.

---

### **2. Identifying an Elementary 3×3 Matrix**

Examples:

#### • Type I (Row Switching):

Swapping row 1 and row 2 of $`I\_3`$:

$`E_1 = \begin{bmatrix} 0 & 1 & 0 \\ 1 & 0 & 0 \\0 & 0 & 1 \end{bmatrix}`$

#### • Type II (Row Scaling):

Multiply row 2 by 3:

$`E_2 = \begin{bmatrix}  1 & 0 & 0 \\ 0 & 3 & 0 \\0 & 0 & 1 \end{bmatrix}`$

#### • Type III (Row Addition):

Add 4 times row 1 to row 3:

$`E_3 = \begin{bmatrix} 1 & 0 & 0 \\0 & 1 & 0 \\4 & 0 & 1 \end{bmatrix}`$

---

### **3. Finding the Inverse of an Elementary 3×3 Matrix**

The inverse of an elementary matrix is also elementary and **corresponds to reversing the row operation**:

* Inverse of Type I (row switch): same matrix

$$
E_1^{-1} = E_1
$$

* Inverse of Type II (row scaling by $k$): scale by $`1/k`$

$$
E_2^{-1} =
\begin{bmatrix}
1 & 0 & 0 \\
0 & \frac{1}{3} & 0 \\
0 & 0 & 1
\end{bmatrix}
$$

* Inverse of Type III (adding $k$ times row $i$ to row $j$): subtract $k$ times row $i$ from row $j$

$$
E_3^{-1} =
\begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
-4 & 0 & 1
\end{bmatrix}
$$

---

### **4. Computing a Product Involving the Inverse of an Elementary 3×3 Matrix**

Let’s compute:

$`E_3^{-1} \cdot A`$

for some $`3 \times 3`$ matrix $`A = [a\_{ij}]`$.

Applying $`E\_3^{-1}`$ corresponds to performing **elementary row operation** on $A$:

* Subtract 4 times row 1 from row 3 of $A$

This is **useful in Gaussian elimination** where:

* A matrix $A$ is row-reduced by premultiplying it by a sequence of elementary matrices.
* The product of the inverses of these matrices gives $A$’s **LU** or **PA = LU** factorizations.

---

### **Summary Table**

| Type | Operation                          | Elementary Matrix                 | Inverse           |
| ---- |------------------------------------|-----------------------------------|-------------------|
| I    | Swap $`R\_i \leftrightarrow R\_j`$ | Row-swap permutation matrix       | Same matrix       |
| II   | Multiply $`R\_i \to k R\_i`$       | Diagonal with $`k`$ at $`(i,i)`$  | Same with $`1/k`$ |
| III  | $`R\_j \to R\_j + k R\_i`$         | Identity with $`k`$ at $`(j,i)`$  | Same with $`-k`$  |

---

