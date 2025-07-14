### **Determinants, Minors, and Cofactors of an $N \times N$ Matrix**

---

### **1. The Determinant of an $N \times N$ Matrix**

The **determinant** of a square matrix is a scalar that captures key properties of the matrix, such as invertibility, volume scaling, and orientation of linear transformations.

For a matrix $A = [a_{ij}]$, the determinant is written as:

* $\det(A)$ or $|A|$

#### Examples:

* **For a $2 \times 2$ matrix**:

$`\det\begin{bmatrix} a & b \\ c & d \end{bmatrix} = ad - bc`$

* **For a $3 \times 3$ matrix**, the determinant can be computed by cofactor expansion or Sarrus' Rule.

For matrices of size $N \geq 4$, determinants are computed **recursively** using **cofactor expansion**.

---

### **2. Minor of an Entry in an $N \times N$ Matrix**

The **minor** of an entry $a_{ij}$, denoted $M_{ij}$, is the determinant of the $(N - 1) \times (N - 1)$ submatrix obtained by removing the $i$-th row and $j$-th column from matrix $A$:

$`M_{ij} = \det(A_{ij})`$

Where $A_{ij}$ is the reduced matrix after removing row $i$ and column $j$.

---

### **3. Cofactor of an Entry**

The **cofactor** of an entry $a_{ij}$, denoted $C_{ij}$, is the signed version of its minor:

$$
C_{ij} = (-1)^{i+j} M_{ij}
$$

This sign alternates in a checkerboard pattern across the matrix.

---

### **4. Determinant Using Cofactor Expansion**

The determinant of matrix $A$ can be computed by expanding along any row or column using the cofactors.

* **Expansion along the $i$-th row**:

$`\det(A) = \sum_{j=1}^{n} a_{ij} \cdot C_{ij}`$

* **Expansion along the $j$-th column**:

$`\det(A) = \sum_{i=1}^{n} a_{ij} \cdot C_{ij}`$

This method is recursive, breaking the calculation into smaller matrices.

---

### **5. Example: Determinant of a $3 \times 3$ Matrix**

Let:

$$
A = \begin{bmatrix} 
1 & 2 & 3 \\
0 & 4 & 5 \\
1 & 0 & 6
\end{bmatrix}
$$

**Step 1: Expand along the first row**

$$
\det(A) = 1 \cdot C_{11} - 2 \cdot C_{12} + 3 \cdot C_{13}
$$

**Step 2: Compute the minors**

* $`M_{11} = \det\begin{bmatrix} 4 & 5 \\ 0 & 6 \end{bmatrix} = 24`$
* $`M_{12} = \det\begin{bmatrix} 0 & 5 \\ 1 & 6 \end{bmatrix} = -5`$
* $`M_{13} = \det\begin{bmatrix} 0 & 4 \\ 1 & 0 \end{bmatrix} = -4`$

**Step 3: Compute the cofactors**

* $C_{11} = (+1) \cdot 24 = 24$
* $C_{12} = (-1) \cdot (-5) = 5$
* $C_{13} = (+1) \cdot (-4) = -4$

**Step 4: Plug into the expansion**

$$
\det(A) = 1(24) - 2(5) + 3(-4) = 24 - 10 - 12 = 2
$$

---

### **Summary**

* **Minor**: Determinant of a submatrix formed by removing a row and a column.
* **Cofactor**: Minor adjusted by a sign factor $(-1)^{i+j}$.
* **Determinant**: Computed by cofactor expansion across any row or column.
* **Recursive**: The determinant of an $N \times N$ matrix reduces to smaller determinants via cofactors.

Determinants are fundamental in linear algebra, used in solving systems of equations (Cramer's Rule), matrix inversion, and analyzing linear transformations.
