### **Finding the Determinant of an $N \times N$ Matrix Using Laplace Expansion**

---

### **1. What Is Laplace Expansion?**

**Laplace expansion** (or **cofactor expansion**) is a method for calculating the **determinant** of a square matrix by expanding along any row or column. It uses **minors** and **cofactors** to break down the computation into smaller parts recursively.

---

### **2. Laplace Expansion Formula**

For an $N \times N$ matrix $A = [a_{ij}]$, the determinant is:

$$
\det(A) = \sum_{j=1}^{n} a_{ij} \cdot C_{ij}
$$

Where:

* $C_{ij} = (-1)^{i+j} \cdot \det(A_{ij})$ is the **cofactor** of $a_{ij}$,
* $A_{ij}$ is the submatrix formed by removing row $i$ and column $j$,
* $\det(A_{ij})$ is the **minor** of $a_{ij}$.

This can also be done along any column $j$:

$$
\det(A) = \sum_{i=1}^{n} a_{ij} \cdot C_{ij}
$$

---

### **3. Example: Determinant of a $3 \times 3$ Matrix**

Let:

$$
A = \begin{bmatrix}
1 & 2 & 3 \\
0 & 4 & 5 \\
1 & 0 & 6
\end{bmatrix}
$$

**Step 1: Expand along the first row**:

$$
\det(A) = 1 \cdot C_{11} - 2 \cdot C_{12} + 3 \cdot C_{13}
$$

**Step 2: Compute cofactors**:

* $`C_{11} = (+1) \cdot \det\begin{bmatrix} 4 & 5 \\ 0 & 6 \end{bmatrix} = 4 \cdot 6 - 0 \cdot 5 = 24`$
* $`C_{12} = (-1) \cdot \det\begin{bmatrix} 0 & 5 \\ 1 & 6 \end{bmatrix} = - (0 \cdot 6 - 1 \cdot 5) = 5`$
* $`C_{13} = (+1) \cdot \det\begin{bmatrix} 0 & 4 \\ 1 & 0 \end{bmatrix} = 0 \cdot 0 - 1 \cdot 4 = -4`$

**Step 3: Plug into formula**:

$$
\det(A) = 1(24) - 2(5) + 3(-4) = 24 - 10 - 12 = 2
$$

---

### **4. Example: Determinant of a $4 \times 4$ Matrix**

Let:

$$
A = \begin{bmatrix}
1 & 0 & 2 & -1 \\
3 & 0 & 0 & 5 \\
2 & 1 & 4 & -3 \\
1 & 0 & 5 & 0
\end{bmatrix}
$$

**Step 1: Expand along the first row** (because it has a zero):

$$
\det(A) = 1 \cdot C_{11} + 0 \cdot C_{12} + 2 \cdot C_{13} + (-1) \cdot C_{14}
$$

We only need to compute $C_{11}$, $C_{13}$, and $C_{14}$:

* **Minor $M_{11}$**:

$$
\det\begin{bmatrix}
0 & 0 & 5 \\
1 & 4 & -3 \\
0 & 5 & 0
\end{bmatrix}
$$

Expanding along the first row:

$$
= 0 \cdot \det(\cdots) - 0 \cdot \det(\cdots) + 5 \cdot \det\begin{bmatrix} 1 & 4 \\ 0 & 5 \end{bmatrix} = 5(1 \cdot 5 - 0 \cdot 4) = 25
$$

So $C_{11} = (+1) \cdot 25 = 25$

* **Minor $M_{13}$**:

$$
\det\begin{bmatrix}
3 & 0 & 5 \\
2 & 1 & -3 \\
1 & 0 & 0
\end{bmatrix}
$$

Expanding along the third column:

$$
= 5 \cdot \det\begin{bmatrix} 2 & 1 \\ 1 & 0 \end{bmatrix} = 5(2 \cdot 0 - 1 \cdot 1) = -5
$$

So $C_{13} = (+1) \cdot (-5) = -5$

* **Minor $M_{14}$**:

$$
\det\begin{bmatrix}
3 & 0 & 0 \\
2 & 1 & 4 \\
1 & 0 & 5
\end{bmatrix}
$$

Expanding along the first row:

$$
= 3 \cdot \det\begin{bmatrix} 1 & 4 \\ 0 & 5 \end{bmatrix} = 3(1 \cdot 5 - 0 \cdot 4) = 15
$$

So $C_{14} = (-1)^1+4 \cdot 15 = (-1)^5 \cdot 15 = -15$

**Step 2: Plug into formula**:

$$
\det(A) = 1(25) + 0 + 2(-5) + (-1)(-15) = 25 - 10 + 15 = 30
$$

---

### **5. Summary**

* Laplace expansion breaks down a determinant into minors and cofactors.
* Expansion can be along **any row or column** — choose one with the most zeros to simplify.
* Recursive and symbolic — best for small or sparse matrices.
* The process uses:

  * **Minors**: Submatrix determinants
  * **Cofactors**: Signed minors $(-1)^{i+j} \cdot \det(A_{ij})$

Laplace expansion is a powerful tool for building intuition and performing manual determinant calculations.
