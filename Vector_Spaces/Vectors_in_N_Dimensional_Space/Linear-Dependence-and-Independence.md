## **Linear Dependence and Independence**

In linear algebra, the concepts of **linear dependence** and **linear independence** help us understand the **structure and span** of vector sets. 
They are crucial for defining **bases**, **dimension**, and solving systems of equations.

---

### **1. Definition of Linear Dependence and Independence**

Let $\{\mathbf{v}_1, \mathbf{v}_2, \dots, \mathbf{v}_k\}$ be vectors in $\mathbb{R}^n$:

* The set is **linearly independent** if the **only** solution to

$$
c_1\mathbf{v}_1 + c_2\mathbf{v}_2 + \dots + c_k\mathbf{v}_k = \mathbf{0}
$$

is $c_1 = c_2 = \dots = c_k = 0$.

* The set is **linearly dependent** if **any nontrivial solution** (not all $c_i = 0$) exists.

This means:

* **Independent**: No vector is a linear combination of the others


* **Dependent**: At least one vector **can** be written as a linear combination of the others

---

### **2. Finding a Vector That Makes a Set Linearly Dependent**

To make a set dependent, you can introduce a vector that is a **linear combination** of existing vectors.

#### **Example:**

Let

$$
\mathbf{v}_1 = \begin{bmatrix} 1 \\ 2 \end{bmatrix}, \quad
\mathbf{v}_2 = \begin{bmatrix} 3 \\ 4 \end{bmatrix}
$$

We want $`\mathbf{v}_3`$ such that the set $\{\mathbf{v}_1, \mathbf{v}_2, \mathbf{v}_3\}$ is **linearly dependent**.

Take:

$$
\mathbf{v}_3 = 2\mathbf{v}_1 + (-1)\mathbf{v}_2 = 2\begin{bmatrix} 1 \\ 2 \end{bmatrix} - \begin{bmatrix} 3 \\ 4 \end{bmatrix}
= \begin{bmatrix} 2 \\ 4 \end{bmatrix} - \begin{bmatrix} 3 \\ 4 \end{bmatrix}
= \begin{bmatrix} -1 \\ 0 \end{bmatrix}
$$

So $`\mathbf{v}_3 = \begin{bmatrix} -1 \\ 0 \end{bmatrix}`$ makes the set dependent.

---

### **3. Identifying Linearly Independent Sets by Inspection**

Some sets can be classified **quickly**:

#### **In $\mathbb{R}^n$:**

* If the set has **more than $n$** vectors ⇒ it is **automatically dependent**



* If any vector is a **zero vector** ⇒ the set is **dependent**



* If one vector is a **multiple** of another ⇒ dependent



#### **Example:**

$$
\begin{bmatrix} 1 \\ 0 \end{bmatrix}, \quad \begin{bmatrix} 2 \\ 0 \end{bmatrix}
\quad \text{→ dependent (same direction)}
$$

$$
\begin{bmatrix} 1 \\ 0 \end{bmatrix}, \quad \begin{bmatrix} 0 \\ 1 \end{bmatrix}
\quad \text{→ independent (orthogonal)}
$$

---

### **4. Identifying Linear Independence Using Row Reduction**

To check independence of vectors $\mathbf{v}_1, \mathbf{v}_2, \dots, \mathbf{v}_k$, form a **matrix** with them as columns:

$$
A = [\mathbf{v}_1\ \mathbf{v}_2\ \dots\ \mathbf{v}_k]
$$

Perform **row reduction (RREF)**:

* If the matrix has **a pivot in every column**, the vectors are **linearly independent**


* If **any column lacks a pivot**, they are **dependent**

---

#### **Example:**

Let:

$$
A = \begin{bmatrix}
1 & 2 & 3 \\
0 & 1 & 2 \\
0 & 0 & 0
\end{bmatrix}
$$

This reduces to:

$$
\begin{bmatrix}
1 & 2 & 3 \\
0 & 1 & 2 \\
0 & 0 & 0
\end{bmatrix}
\Rightarrow \text{Only 2 pivots → dependent}
$$

Because one column lacks a pivot, one vector is a linear combination of the others.

---

### **Summary Table**

| Scenario                                       | Result                   |
| ---------------------------------------------- | ------------------------ |
| All $c_i = 0$ is the only solution             | **Linearly Independent** |
| At least one nonzero $c_i$ solves the equation | **Linearly Dependent**   |
| Any vector = combination of others             | **Dependent**            |
| RREF has a pivot in every column               | **Independent**          |
| RREF has fewer pivots than columns             | **Dependent**            |
| Zero vector included                           | **Always Dependent**     |

---

### **Conclusion**

Linear independence is fundamental to:

* Defining **basis and dimension**


* Testing **invertibility** of matrices


* Understanding **span** and **vector spaces**


Being able to quickly assess dependence—visually, algebraically, or via row operations—is a powerful skill in linear algebra and applied mathematics.
