## **Basic Properties of Determinants**

The **determinant** of a matrix provides critical information about linear transformations, 
systems of equations, and geometric interpretations such as **volume**, **orientation**, 
and **invertibility**. This deep dive covers foundational properties and how to apply them in 
computations and geometry.

---

### **1. Determinant of a Triangular Matrix**

A **triangular matrix** (either upper or lower) is one where all entries **above or below** the main diagonal are zero.

If:

$$
T = \begin{bmatrix}
t_{11} & * & * \\
0 & t_{22} & * \\
0 & 0 & t_{33}
\end{bmatrix}
$$

Then:

$$
\det(T) = t_{11} \cdot t_{22} \cdot t_{33}
$$

**Key Rule**: The determinant of a triangular matrix is simply the **product of its diagonal elements**.

---

### **2. Determinant of a Matrix with Many Zeros**

A matrix with many zeros, especially in a row or column, can often be simplified quickly using **cofactor expansion**.

**Best strategy**: Expand along a row or column with the **most zeros** to reduce computation.

**Example:**

$$
A = \begin{bmatrix}
0 & 0 & 5 \\
0 & 1 & 2 \\
0 & 3 & 4
\end{bmatrix}
$$

Expand along the **first row**:

$$
\det(A) = 5 \cdot (-1)^{1+3} \cdot \det\begin{bmatrix} 0 & 1 \\ 0 & 3 \end{bmatrix}
= 5 \cdot (1) \cdot (0 \cdot 3 - 0 \cdot 1) = 5 \cdot 0 = 0
$$

A zero row or linearly dependent rows always yield a **zero determinant**.

---

### **3. Volume of an $n$-Dimensional Parallelepiped**

The determinant of a matrix formed by **column vectors** $\mathbf{v}_1, \mathbf{v}_2, \dots, \mathbf{v}_n$ gives the **signed volume** of the **parallelepiped** spanned by these vectors:

Let $`A = [\mathbf{v}_1 \ \mathbf{v}_2 \ \dots \ \mathbf{v}_n]`$. Then:

$$
\text{Volume} = |\det(A)|
$$

The **absolute value** ensures volume is non-negative, even if the determinant is negative(due to orientation).

---

### **4. Calculating Expressions Involving Given Determinants and Matrix Types**

Several determinant properties help in computing expressions quickly:

#### **a. Determinant of a scalar multiple of a matrix**

If $A$ is $n \times n$, and $k$ is a scalar:

$$
\det(kA) = k^n \cdot \det(A)
$$



#### **b. Determinant of a product**

$$
\det(AB) = \det(A) \cdot \det(B)
$$



#### **c. Determinant of an inverse**

If $A$ is invertible:

$$
\det(A^{-1}) = \frac{1}{\det(A)}
$$



#### **d. Determinant of a transpose**

$$
\det(A^T) = \det(A)
$$

---


### **Example Problem**

Let:

* $`\det(A) = 3`$
* $`\det(B) = -2`$
* $A$ is $`3 \times 3`$

Then:

* $`\det(2A) = 2^3 \cdot \det(A) = 8 \cdot 3 = 24`$
* $`\det(A^T B^{-1}) = \det(A^T) \cdot \det(B^{-1}) = \det(A) \cdot \frac{1}{\det(B)} = \frac{3}{-2} = -\frac{3}{2}`$

---


### **5. Summary of Key Properties**

| Property                              | Formula                                                    |                                            
| ------------------------------------- |------------------------------------------------------------|  
| Determinant of triangular matrix      | Product of diagonal entries                                |                                             
| Determinant of matrix with zero row   | Zero                                                       |                                             
| Determinant of matrix with many zeros | Expand along sparse row/column                             |                                              
| Determinant of $kA$                   | $k^n \cdot \det(A)$                                        |                                              
| Determinant of $AB$                   | $\det(A) \cdot \det(B)$                                    |                                              
| Determinant of $A^T$                  | $\det(A)$                                                  |                                             
| Determinant of $A^{-1}$               | $\frac{1}{\det(A)}$                                        |                                            
| Volume of parallelepiped from vectors | $`(\mid \det([\mathbf{v}\_1 \dots \mathbf{v}\_n]) \mid)`$  | 

---

Determinants encode both **algebraic structure** and **geometric meaning**, making them a central tool in linear algebra for simplification, transformation, and analysis.
