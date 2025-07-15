## **LU Factorization of 2×2 Matrices**

---

### **1. What Is LU Factorization?**

**LU Factorization** expresses a square matrix $A$ as a product of:

* A **lower triangular matrix** $L$


* An **upper triangular matrix** $U$


$$
A = LU
$$

Where:

* $L$ has 1s on the diagonal and possibly nonzero entries below the diagonal.


* $U$ is upper triangular (zeros below the diagonal).

---

### **2. General Form for 2×2 LU Factorization**

Let:

$`A = \begin{bmatrix} a & b \\c & d \end{bmatrix}`$

We seek:

$`L = \begin{bmatrix} 1 & 0 \\\ell & 1 \end{bmatrix}, \quad U = \begin{bmatrix} u_{11} & u_{12} \\0 & u_{22} \end{bmatrix}`$

Then:

$`LU = \begin{bmatrix} 1 & 0 \\\ell & 1 \end{bmatrix} \begin{bmatrix} u_{11} & u_{12} \\0 & u_{22} \end{bmatrix}= \begin{bmatrix} u_{11} & u_{12} \\\ell u_{11} & \ell u_{12} + u_{22} \end{bmatrix}`$

Set this equal to $A$ to solve:

* $`u_{11} = a`$


* $`u_{12} = b`$


* $`\ell u_{11} = c \Rightarrow \ell = \frac{c}{a}`$ (if $`a \ne 0`$)


* $`\ell u_{12} + u_{22} = d \Rightarrow u_{22} = d - \frac{c}{a} b`$

---

### **3. Example: LU Factorization of a 2×2 Nonsingular Matrix**

Let:

$`A = \begin{bmatrix} 2 & 3 \\4 & 7 \end{bmatrix}`$

Step-by-step:

* $`u_{11} = 2`$


* $`u_{12} = 3`$


* $`\ell = \frac{4}{2} = 2`$


* $`u_{22} = 7 - 2 \cdot 3 = 1`$

So:

$`L = \begin{bmatrix} 1 & 0 \\2 & 1 \end{bmatrix}, \quad U = \begin{bmatrix} 2 & 3 \\0 & 1 \end{bmatrix} \Rightarrow A = LU`$

---

### **4. Identifying LU Factorizations**

If given two matrices $`L`$ and $`U`$, check:

* $`L`$ must be lower triangular with 1s on the diagonal.


* $`U`$ must be upper triangular.


* Multiplying them must reconstruct the original matrix.

---

### **5. LU Factorization of a Singular 2×2 Matrix**

Suppose:

$`A = \begin{bmatrix} 2 & 4 \\1 & 2 \end{bmatrix}`$

Note: $`\det(A) = 2 \cdot 2 - 4 \cdot 1 = 0 \Rightarrow`$ Singular.

Try LU:

* $`u_{11} = 2`$


* $`u_{12} = 4`$


* $`\ell = \frac{1}{2}`$


* $`u_{22} = 2 - \frac{1}{2} \cdot 4 = 0`$

So:

$`L = \begin{bmatrix} 1 & 0 \\\frac{1}{2} & 1 \end{bmatrix}, \quad U = \begin{bmatrix} 2 & 4 \\0 & 0 \end{bmatrix}`$

✅ LU factorization exists, though **$U$** is **singular** (zero determinant). Not invertible, but the factorization is valid.

---

### **6. When Does LU Factorization Fail?**

* LU factorization **without pivoting** may fail if the top-left pivot element is **zero** (i.e., $`a = 0`$) in:

$`\begin{bmatrix} a & b \\c & d \end{bmatrix}`$

* In such cases, **row exchanges** (i.e., **LU with partial pivoting**) may be needed: $`PA = LU`$, where $P$ is a permutation matrix.

---

### Summary

| Topic                        | Key Idea                                                                |
| ---------------------------- |-------------------------------------------------------------------------|
| LU Factorization             | Factor a matrix into a lower and upper triangular matrix                |
| Form for 2×2 Matrix          | $`A = LU`$ where $`L = \begin{bmatrix}1 & 0 \\ \ell & 1 \end{bmatrix}`$ |
| Valid for Singular Matrices? | Yes — though $U$ will be singular (zero determinant)                    |
| LU Fails When                | Leading pivot (e.g., $a$) is zero and no row swap is used               |
| Pivoting Fixes Breakdown     | Use row permutations to enable LU for all nonsingular matrices          |

LU decomposition is a foundation for solving linear systems, matrix inversion, and understanding numerical stability in algorithms.
