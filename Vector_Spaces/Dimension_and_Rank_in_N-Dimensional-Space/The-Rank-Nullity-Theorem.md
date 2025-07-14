## **The Rank-Nullity Theorem**

---

### **1. The Rank-Nullity Theorem: Core Statement**

For any $`m \times n`$ matrix $A$, the **Rank-Nullity Theorem** states:

$$
\boxed{\text{rank}(A) + \text{nullity}(A) = n}
$$

Where:

* $`\text{rank}(A) = \dim(\text{Col}(A))`$: number of linearly independent columns (pivot columns)


* $`\text{nullity}(A) = \dim(\text{Null}(A))`$: number of free variables (dimension of the null space)


* $n$: number of columns in $A$


This theorem connects the **structure of solutions to the linear system** $`A\mathbf{x} = \mathbf{0}`$ 
with the **column space** and the **dimension of the domain** of $A$.

---

### **2. Finding the Rank or Nullity Using the Rank-Nullity Theorem**

#### **Example 1**: Given a matrix

Let:

$$
A = \begin{bmatrix}
1 & 2 & 3 \\
0 & 1 & 4 \\
0 & 0 & 0 \\
\end{bmatrix}
$$

From row-reduction:

* Rank = number of pivot columns = 2


* $`n = 3`$ (3 columns)

$$
\text{nullity}(A) = n - \text{rank}(A) = 3 - 2 = \boxed{1}
$$

So the null space is 1-dimensional.

---

#### **Example 2**: Given only rank

If $A$ is a $`5 \times 7`$ matrix and rank$`(A) = 4`$, then:

$$
\text{nullity}(A) = 7 - 4 = \boxed{3}
$$

So the solution space of $`A\mathbf{x} = \mathbf{0}`$ has dimension 3.

---

### **3. Finding the Rank or Nullity Given Column or Null Space Descriptions**

#### **Example 3**: Given null space description

If $`\text{Null}(A)`$ is spanned by:

$`\left\{ \begin{bmatrix} 1 \\ 0 \\ 1 \\ 0 \end{bmatrix}, \begin{bmatrix} 0 \\ 1 \\ -1 \\ 0 \end{bmatrix} \right\} \Rightarrow \text{nullity}(A) = 2`$

And $A$ has 4 columns $`\Rightarrow n = 4`$, so:

$$
\text{rank}(A) = 4 - 2 = \boxed{2}
$$

---

#### **Example 4**: Given column space description

If the column space of $`A \in \mathbb{R}^{3 \times 5}`$ is spanned by 3 vectors, then:

$`\text{rank}(A) = 3,\quad \text{nullity}(A) = 5 - 3 = \boxed{2}`$

---

### **4. Identifying True Statements Using the Invertible Matrix Theorem and Rank-Nullity Theorem**

#### **The Invertible Matrix Theorem** (for square $n \times n$ matrices) says the following are equivalent:

| Property                                             | Interpretation                                           |
| ---------------------------------------------------- |----------------------------------------------------------|
| $A$ is invertible                                    | The matrix has full rank $n$                             |
| Columns of $A$ are linearly independent              | Null space is trivial $`\Rightarrow \text{nullity} = 0`$ |
| $`A\mathbf{x} = \mathbf{0}`$ has only trivial solution | Unique solution implies nullity = 0                      |
| $A$ has pivot in every row and column                | Rank = $n$                                               |
| Columns span $`\mathbb{R}^n`$                          | Column space is full                                     |

#### **Using Rank-Nullity + Invertibility: True Statements**

* If $`\text{nullity}(A) = 0`$, then **$A$ has full rank** $`\Rightarrow`$ invertible if square


* If $`\text{rank}(A) = n`$, then columns are linearly independent


* If $`\text{nullity}(A) > 0`$, then $A$ is **not invertible**


* If $`\text{rank}(A) < n`$, then columns are **linearly dependent**

---

### **5. Summary Table**

| Quantity                   | Formula / Property                                         |
| -------------------------- | ---------------------------------------------------------- |
| **Rank**                   | Number of pivot columns                                    |
| **Nullity**                | $`n - \text{rank}(A)`$                                       |
| **Rank-Nullity Theorem**   | $`\text{rank}(A) + \text{nullity}(A) = n`$                   |
| **Invertibility (square)** | $`\text{rank}(A) = n \Leftrightarrow \text{nullity}(A) = 0`$ |
| **Full rank, non-square**  | Max possible rank = min(rows, cols)                        |

---

### ✅ Key Insights:

* **Rank measures constraints**, **nullity measures freedom**.
* Rank-nullity theorem bridges **algebraic structure** (solutions) and **geometric structure** (dimension).
* Critical in solving linear systems, analyzing transformations, and checking invertibility.
