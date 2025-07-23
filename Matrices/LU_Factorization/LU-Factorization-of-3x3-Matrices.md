## **LU Factorization of 3x3 Matrices**

LU factorization (or LU decomposition) expresses a square matrix as the product of a **lower triangular matrix** $L$ and an **upper triangular matrix** $U$, 
such that:

$`A = LU`$


This decomposition is foundational in numerical linear algebra, particularly in solving linear systems and computing matrix inverses.

---

### 1. **Finding the LU Factorization Using a Single Elementary Row Operation**

If matrix $`A \in \mathbb{R}^{3 \times 3}`$ can be reduced to upper triangular form in **one row operation**, the LU factorization can be obtained as follows:

* Let $`E`$ be the elementary matrix corresponding to that row operation.


* Then:

$`EA = U \quad \Rightarrow \quad A = E^{-1}U`$


* So, the LU factorization is:


$`L = E^{-1}, \quad U = EA`$


**Example**
Let:


$`A = \begin{bmatrix} 1 & 2 & 3 \\4 & 5 & 6 \\7 & 8 & 9 \end{bmatrix}`$


Apply one row operation:


$`R_2 \gets R_2 - 4R_1`$, corresponding to elementary matrix:


$`E = \begin{bmatrix} 1 & 0 & 0 \\-4 & 1 & 0 \\0 & 0 & 1 \end{bmatrix}`$


Then:


* $`U = EA`$


* $`L = E^{-1}`$, which in this case is:


$`L = \begin{bmatrix} 1 & 0 & 0 \\4 & 1 & 0 \\0 & 0 & 1 \end{bmatrix}`$


---

### 2. **Finding the Lower Triangular Matrix Given the Elementary Row Operations**

Each **elementary row operation** applied to reduce a matrix to upper triangular form corresponds to **left multiplication by an elementary matrix**.

* Track each operation:

  * If $`E_1, E_2, \dots, E_k`$ are the elementary matrices such that:

    $`E_k \dots E_2E_1A = U`$


* Then:

  $`A = E_1^{-1}E_2^{-1} \dots E_k^{-1} U`$

  and:

  $`L = E_1^{-1}E_2^{-1} \dots E_k^{-1}`$


Since inverses of elementary matrices that subtract multiples of one row from another are lower triangular, their product $L$ is also lower triangular.

---

### 3. **Finding the LU Factorization Using Two or More Elementary Row Operations**

With multiple steps, keep track of all the operations used to zero out entries **below the pivot positions**:

* For a 3×3 matrix $A$:

  1. Apply row operations to zero out $`a_{21}`$ and $`a_{31}`$
  

  2. Apply row operations to zero out $`a_{32}`$


Each step corresponds to left multiplication by a **lower triangular matrix**. Denote:

* $`E_1, E_2`$ for operations on column 1,


* $`E_3`$ for operations on column 2.

Then:

$`E_3E_2E_1A = U \quad \Rightarrow \quad A = E_1^{-1}E_2^{-1}E_3^{-1}U`$


So:

* $`L = E_1^{-1}E_2^{-1}E_3^{-1}`$


* $`A = LU`$

---

### Summary Table

| Task                  | Key Idea                                                    | Expression                      |
| --------------------- |-------------------------------------------------------------|---------------------------------|
| Single Operation      | One row operation gives $`E`$, then $`A = E^{-1}U`$         | $`L = E^{-1}`$, $`U = EA`$      |
| Multiple Operations   | Track sequence of $`E_i`$, invert & multiply                | $`L = (E_k \dots E_1)^{-1}`$    |
| Lower Matrix from Ops | Each row operation corresponds to a lower triangular matrix | $`L = E_1^{-1} \dots E_k^{-1}`$ |

LU factorization without pivoting assumes no row swaps are needed. For numerical stability, pivoting strategies like **PA = LU** may be used.
