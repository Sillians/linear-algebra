## **Further Properties of Determinants**

The **determinant** is a scalar value that reveals crucial properties of a square matrix, such as **invertibility**, **volume scaling**, and **singularity**. 
Beyond basic row operations and expansion rules, several deeper properties allow efficient computation and reasoning about matrices.

---

### **1. Determinant of a Product**

For square matrices $A$ and $B$ of the same size:

$$
\boxed{\det(AB) = \det(A) \cdot \det(B)}
$$

This means the determinant of a matrix product equals the product of the determinants.

#### **Example:**

Let

$$
A = \begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix}, \quad
B = \begin{bmatrix} 0 & 1 \\ 1 & 0 \end{bmatrix}
$$

Then:

* $`\det(A) = (1)(4) - (2)(3) = -2`$
* $`\det(B) = (0)(0) - (1)(1) = -1`$
* $`\det(AB) = (-2)(-1) = \boxed{2}`$

This also reflects how the **volume scaling** by one transformation (via $A$) is multiplied by that of another (via $B$).

---

### **2. Determinant of the Inverse of a Matrix**

If $A$ is an invertible square matrix, then:

$$
\boxed{\det(A^{-1}) = \frac{1}{\det(A)}}
$$

This property follows from the rule $`\det(AA^{-1}) = \det(I) = 1`$.

#### **Example:**

Let $`\det(A) = 5 \Rightarrow \det(A^{-1}) = \frac{1}{5}`$

---

### **3. Determinant of a Transpose**

$$
\boxed{\det(A^T) = \det(A)}
$$

The determinant is **unchanged** under transposition. This is useful when row operations are more convenient than column operations (or vice versa).

---

### **4. Determinant of a Scalar Multiple**

If $A$ is an $`n \times n`$ matrix and $`c \in \mathbb{R}`$, then:

$$
\boxed{\det(cA) = c^n \cdot \det(A)}
$$

#### **Example:**

Let $`A \in \mathbb{R}^{3 \times 3}`$, $`\det(A) = 2`$, then:

$$
\det(5A) = 5^3 \cdot 2 = 125 \cdot 2 = 250
$$

---

### **5. Calculating a Determinant Using Linearity**

The determinant is **linear in each row or column** when others are fixed. This means:

* You can **factor constants** out of a row or column.
* If a row/column is a **sum**, you can **split the determinant** accordingly.

#### **Example:**

Let:

$` A = \begin{bmatrix}  1 + 2 & b \\ c & d  \end{bmatrix} =  \begin{bmatrix}  1 & b \\ c & d  \end{bmatrix} +  \begin{bmatrix}  2 & 0 \\ 0 & 0  \end{bmatrix}`$

Then:

$` \det(A) = \det\left(\begin{bmatrix}  1 & b \\ c & d  \end{bmatrix}\right) +  \det\left(\begin{bmatrix}  2 & 0 \\ 0 & 0  \end{bmatrix}\right) = (1)(d) - (b)(c) + 0 = d - bc`$

Linearity is powerful for simplifying determinants where symbolic components or sums are involved.

---

###  **Summary of Key Properties**

| Property                       | Formula                               |
| ------------------------------ | ------------------------------------- |
| Determinant of product         | $\det(AB) = \det(A)\det(B)$           |
| Determinant of inverse         | $\det(A^{-1}) = \frac{1}{\det(A)}$    |
| Determinant of transpose       | $\det(A^T) = \det(A)$                 |
| Determinant of scalar multiple | $\det(cA) = c^n \cdot \det(A)$        |
| Linearity in rows/columns      | Can split and factor out rows/columns |

---

### **Conclusion**

These advanced properties of determinants help:

* Simplify calculations across transformations,
* Understand matrix behavior under operations,
* Efficiently assess invertibility and volume scaling.

They are essential in deeper applications like eigenvalue problems, diagonalization, and system solvability.
