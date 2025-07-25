## **LU Factorization of $`n \times n`$ Matrices**

LU factorization (or LU decomposition) expresses a square matrix $`A \in \mathbb{R}^{n \times n}`$ as the product:

$`A = LU`$

where:

* $`L`$ is a **lower triangular matrix** with unit diagonal entries ($`l_{ii} = 1`$)


* $`U`$ is an **upper triangular matrix**


LU factorization is central to solving systems of equations, computing determinants, and inverting matrices efficiently.

---

###  Finding Missing Numbers in the Matrix $U$ of an LU Factorization

Given:

* A full matrix $`A`$,


* A partially filled $`L`$, and

* A partially filled upper triangular matrix $`U`$


To find the missing values in $`U`$, solve:

$`A = LU`$

Match corresponding entries in $`A`$ with those from multiplying $`L`$ and $`U`$. Use matrix multiplication:


$`a_{ij} = \sum_{k=1}^{i} l_{ik} u_{kj}`$


This works because in LU decomposition, the structure of $L$ limits summation to $`k \leq i`$, and $`U`$ 
contributes only for $`k \leq j`$.

---

### Finding Missing Numbers in the Matrix $`L`$ of an LU Factorization

Same approach as above, but solve for entries in $`L`$, using:


$`a_{ij} = \sum_{k=1}^{j} l_{ik} u_{kj}`$


This formula ensures you use only known values in the lower triangular matrix and known $`U`$ entries to
solve for unknowns in $`L`$.

---

###  Finding the LU Factorization of a $`3 \times 3`$ Matrix

Let

$`A = \begin{bmatrix} a_{11} & a_{12} & a_{13} \\a_{21} & a_{22} & a_{23} \\a_{31} & a_{32} & a_{33} \end{bmatrix}`$


Step-by-step:

1. Perform Gaussian elimination to zero out entries below the diagonal of $`A`$.


2. Each row operation corresponds to an elementary lower triangular matrix.


3. Combine inverses of these operations to construct $`L`$, and the final form of $`A`$ is $`U`$.



For example:

* Subtracting $`\frac{a_{21}}{a_{11}} \cdot \text{Row}_1`$ from Row$`_2`$ affects $`L`$'s second row.


* Continue elimination for lower entries in the 3rd column.

---

### Finding the LU Factorization of a $`4 \times 4`$ Matrix

Follow the same procedure as for $`3 \times 3`$, extending to more steps:

1. Eliminate below the pivot in column 1 (entries $`a_{21}, a_{31}, a_{41}`$)


2. Move to column 2 and eliminate $`a_{32}, a_{42}`$


3. Eliminate $`a_{43}`$ in column 3


Each elimination contributes to entries in $`L`$, while the remaining entries after all operations form $`U`$. 
Ensure pivots are non-zero (use partial pivoting if needed).

---

### Summary Table

| Step | Objective                                   | Method                                |
| ---- |---------------------------------------------| ------------------------------------- |
| 1    | Decompose matrix $`A`$ into $`L`$ and $`U`$ | Gaussian elimination                  |
| 2    | Solve for missing entries in $`L`$ or $`U`$ | Use matrix multiplication constraints |
| 3    | Construct full $`L`$ and $`U`$              | Apply row operation coefficients      |
| 4    | Verify result                               | Confirm $`A = LU`$                      |

LU factorization is foundational in numerical linear algebra, enabling faster solutions of systems like
$`Ax = b`$ by forward and backward substitution.
