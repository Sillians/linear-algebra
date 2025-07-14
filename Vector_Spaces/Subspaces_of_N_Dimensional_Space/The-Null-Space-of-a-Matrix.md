## **The Null Space of a Matrix**

---

## **Definition**

The **null space** (also known as the **kernel**) of a matrix $A$ is the set of all vectors $`\mathbf{x}`$ such that:

$$
A\mathbf{x} = \mathbf{0}
$$

If $A$ is an $`m \times n`$ matrix, then the null space of $A$ is a **subspace** of $`\mathbb{R}^n`$.

---

## **1. Identifying Whether a Vector Lies in the Null Space of a Given Matrix**

To determine if a vector $`\mathbf{x} \in \mathbb{R}^n`$ lies in the null space of matrix $A$, perform the matrix-vector multiplication:

$$
A\mathbf{x}
$$

If the result is the zero vector $`\mathbf{0}`$, then $`\mathbf{x} \in \text{Null}(A)`$.

### **Example**

Let:

$`A = \begin{bmatrix} 1 & 2 \\ 3 & 6 \end{bmatrix}, \quad \mathbf{x} = \begin{bmatrix} 2 \\ -1 \end{bmatrix}`$

Then:

$`A\mathbf{x} = \begin{bmatrix} 1 & 2 \\ 3 & 6 \end{bmatrix} \begin{bmatrix} 2 \\ -1 \end{bmatrix} = \begin{bmatrix} 0 \\ 0 \end{bmatrix}`$

So, $`\mathbf{x} \in \text{Null}(A)`$.

---

## **2. Solve a Variable in a Vector Lying in the Null Space of a Given Matrix**

Suppose a vector $`\mathbf{x} = \begin{bmatrix} x_1 \\ x_2 \\ x_3 \end{bmatrix}`$ lies in the null space of matrix $A$. Then solving:

$$
A\mathbf{x} = \mathbf{0}
$$

yields linear equations, which can be used to express some variables in terms of others (free variables).

### **Example**

Let:

$`A = \begin{bmatrix} 1 & -1 & 2 \\ 2 & -2 & 4 \end{bmatrix}`$

Solve $`A\mathbf{x} = \mathbf{0}`$:

Row reduce:

$`\begin{bmatrix} 1 & -1 & 2 \\ 2 & -2 & 4 \end{bmatrix} \rightarrow \begin{bmatrix} 1 & -1 & 2 \\ 0 & 0 & 0 \end{bmatrix}`$

From the first row:

$`x_1 - x_2 + 2x_3 = 0 \Rightarrow x_1 = x_2 - 2x_3`$

So the null space is:

$`\text{Null}(A) = \left\{ \begin{bmatrix} x_2 - 2x_3 \\ x_2 \\ x_3 \end{bmatrix} : x_2, x_3 \in \mathbb{R} \right\}`$

---

## **3. Finding the Null Space of a Given Matrix**

To find the null space of a matrix $A$:

1. Set up and solve the homogeneous equation $`A\mathbf{x} = \mathbf{0}`$.


2. Use row reduction to find the solution space.


3. Express the solution in parametric vector form.


### **Example**

Let:

$`A = \begin{bmatrix} 1 & 2 & 1 \\ 0 & 0 & 1 \end{bmatrix}`$

Solve $`A\mathbf{x} = \mathbf{0}`$. Let $`\mathbf{x} = \begin{bmatrix} x_1 \\ x_2 \\ x_3 \end{bmatrix}`$.

From row 2:

$$
x_3 = 0
$$

From row 1:

$$
x_1 + 2x_2 + x_3 = 0 \Rightarrow x_1 = -2x_2
$$

Let $x_2 = t$. Then:

$`\mathbf{x} = \begin{bmatrix} -2t \\ t \\ 0 \end{bmatrix} = t \begin{bmatrix} -2 \\ 1 \\ 0 \end{bmatrix}`$

So:

$`\text{Null}(A) = \text{span} \left\{ \begin{bmatrix} -2 \\ 1 \\ 0 \end{bmatrix} \right\}`$

---

## **Key Properties of the Null Space**

* The null space is a **subspace** of $`\mathbb{R}^n`$.


* The **nullity** of matrix $A$ is the **dimension** of $`\text{Null}(A)`$.


* **Rank–Nullity Theorem**:


$$
\text{rank}(A) + \text{nullity}(A) = n
$$

where $n$ is the number of columns of $A$.
