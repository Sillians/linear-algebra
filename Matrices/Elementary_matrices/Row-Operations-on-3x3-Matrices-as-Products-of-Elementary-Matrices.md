## **Row Operations on 3×3 Matrices as Products of Elementary Matrices**

In linear algebra, every row operation performed on a matrix can be expressed as a left multiplication by 
an *elementary matrix*. This allows one to systematically transform a 3×3 matrix using matrix multiplication 
instead of step-by-step row manipulation. Understanding this principle is crucial for matrix factorizations, 
solving systems of equations, and computing inverses.

---

### **Types of Elementary Row Operations and Corresponding Elementary Matrices**

Each elementary row operation corresponds to a specific elementary matrix:

| Row Operation Type | Description                             | Elementary Matrix Form                                    |
| ------------------ |-----------------------------------------|-----------------------------------------------------------|
| Row Swap           | Swap rows $i$ and $j$                   | Identity matrix with rows $i$ and $j$ swapped             |
| Row Scaling        | Multiply row $i$ by scalar $`k \neq 0`$ | Identity matrix with $i$th diagonal entry replaced by $k$ |
| Row Replacement    | Add $k$ times row $j$ to row $i$        | Identity matrix with $k$ in the $`(i, j)`$ position       |

---

### **1. Finding the Row Operation Equivalent To Left Multiplication by an Elementary Matrix**

To determine the row operation that corresponds to left multiplication by an elementary matrix $E$:


* **Interpret the transformation:** See how $E$ modifies the identity matrix.


* **Analyze the effect:** Compare $`E \cdot I`$ to identify if rows were swapped, scaled, or combined.


**Example:**
If

$`E = \begin{bmatrix} 1 & 0 & 0 \\2 & 1 & 0 \\0 & 0 & 1 \end{bmatrix},`$


then multiplying a 3×3 matrix $A$ by $E$ on the left adds 2 times row 1 to row 2.

---

### **2. Finding the Matrix Left Multiplication Equivalent To a Given Row Operation**

To write a row operation as a matrix:


* Start with the identity matrix $`I_3`$.


* Apply the row operation to $`I_3`$.


* The resulting matrix is the elementary matrix.




**Example:**


To represent “swap row 1 and row 3,” apply the swap to $`I_3`$:


$`E = \begin{bmatrix} 0 & 0 & 1 \\0 & 1 & 0 \\1 & 0 & 0 \end{bmatrix}`$

---

### **3. Finding the Matrix Left Multiplication Equivalent To a Sequence of Row Operations**

To apply multiple row operations:


* Convert each row operation to its corresponding elementary matrix $`E_1, E_2, \ldots, E_k`$.


* The combined effect is the product $`E_k \cdots E_2 E_1`$, applied left-to-right.


**Example:**
Suppose the row operations are:

1. Multiply row 2 by 3


2. Add 2 × row 1 to row 2

Then,

$`E_1 = \begin{bmatrix} 1 & 0 & 0 \\0 & 3 & 0 \\0 & 0 & 1 \end{bmatrix}, \quad E_2 = \begin{bmatrix} 1 & 0 & 0 \\2 & 1 & 0 \\0 & 0 & 1 \end{bmatrix}`$


The total transformation matrix is $`E_2 E_1`$.

---

### **Conclusion**

Every sequence of row operations on a 3×3 matrix can be encoded as multiplication by a product of elementary 
matrices. This representation is crucial for algorithmic approaches to matrix inversion, LU decomposition, and Gaussian elimination.
