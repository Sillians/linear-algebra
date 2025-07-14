## **Finding a Basis of the Null Space of a Matrix**

---

## **Overview**

The **null space** (or kernel) of a matrix $`A \in \mathbb{R}^{m \times n}`$ is the set of all vectors $`\mathbf{x} \in \mathbb{R}^n`$ such that:

$$
A\mathbf{x} = \mathbf{0}
$$

The **basis of the null space** is a set of **linearly independent** vectors that span this space.

---

## **1. Finding a Basis for a Given Null Space**

To find a basis:

1. Solve the homogeneous system $`A\mathbf{x} = \mathbf{0}`$.


2. Express the solution in parametric vector form.


3. The vectors multiplied by free parameters form the basis.


**Example:**

$`A = \begin{bmatrix} 1 & 2 & 3 \\0 & 0 & 0 \end{bmatrix} \Rightarrow \text{Row reduce to: } \begin{bmatrix} 1 & 2 & 3 \\0 & 0 & 0 \end{bmatrix}`$

Set:

$`x_1 + 2x_2 + 3x_3 = 0 \Rightarrow x_1 = -2x_2 - 3x_3`$

Solution:

$`\mathbf{x} = x_2\begin{bmatrix} -2 \\ 1 \\ 0 \end{bmatrix} + x_3\begin{bmatrix} -3 \\ 0 \\ 1 \end{bmatrix} \Rightarrow \text{Basis} = \left\{ \begin{bmatrix} -2 \\ 1 \\ 0 \end{bmatrix}, \begin{bmatrix} -3 \\ 0 \\ 1 \end{bmatrix} \right\}`$

---

## **2. Finding a Basis for the Null Space of a Matrix Given in Reduced Row Echelon Form (RREF)**

### Steps:

1. Identify pivot (leading 1) and free variables.


2. Express pivot variables in terms of free variables.


3. Write the solution vector in terms of free variables.


4. Vectors attached to each free variable form the basis.


**Example:**

$`A_{rref} = \begin{bmatrix} 1 & 0 & -2 & 1 \\0 & 1 & 1 & -3 \end{bmatrix}`$


Variables: $`x_1, x_2`$ are pivot; $`x_3, x_4`$ are free.

Solve:

* $`x_1 = 2x_3 - x_4`$


* $`x_2 = -x_3 + 3x_4`$

Solution:

$`\mathbf{x} = x_3\begin{bmatrix} 2 \\ -1 \\ 1 \\ 0 \end{bmatrix} + x_4\begin{bmatrix} -1 \\ 3 \\ 0 \\ 1 \end{bmatrix} \Rightarrow \text{Basis} = \left\{ \begin{bmatrix} 2 \\ -1 \\ 1 \\ 0 \end{bmatrix}, \begin{bmatrix} -1 \\ 3 \\ 0 \\ 1 \end{bmatrix} \right\}`$

---

## **3. Finding a Basis of the Null Space of a Matrix Given a Row Equivalent Matrix**

If $`A \sim B`$ (i.e., $B$ is row equivalent to $A$), then they have the **same null space**.

### Steps:

1. Use the row-reduced (or partially row-reduced) matrix.


2. Proceed as in the previous section to extract the null space.


3. This is valid because elementary row operations preserve the null space.

---

## **4. Finding a Basis for the Null Space of a Matrix That Is Not in Reduced Row Echelon Form**

### Steps:

1. Perform **Gaussian elimination** (or Gauss-Jordan) to reduce the matrix to RREF or row echelon form.


2. Use back-substitution to solve $`A\mathbf{x} = \mathbf{0}`$.


3. Identify free variables and construct the solution space.

**Example:**

$`A = \begin{bmatrix} 2 & 4 & 6 \\1 & 2 & 3 \end{bmatrix}`$

Row reduce:

$`\begin{bmatrix} 1 & 2 & 3 \\0 & 0 & 0 \end{bmatrix} \Rightarrow x_1 + 2x_2 + 3x_3 = 0 \Rightarrow x_1 = -2x_2 - 3x_3`$

Then:

$`\mathbf{x} = x_2\begin{bmatrix} -2 \\ 1 \\ 0 \end{bmatrix} + x_3\begin{bmatrix} -3 \\ 0 \\ 1 \end{bmatrix} \Rightarrow \text{Basis} = \left\{ \begin{bmatrix} -2 \\ 1 \\ 0 \end{bmatrix}, \begin{bmatrix} -3 \\ 0 \\ 1 \end{bmatrix} \right\}`$

---

## **Key Concepts Recap**

| **Concept**                 | **Description**                                      |
| --------------------------- | ---------------------------------------------------- |
| **Null space**              | Set of solutions to $`A\mathbf{x} = 0`$                |
| **Basis**                   | Linearly independent vectors spanning the null space |
| **Free variables**          | Correspond to columns without pivots                 |
| **Number of basis vectors** | $`n - \text{rank}(A)`$, where $`n`$ is number of columns |

---

## **Conclusion**

Finding the basis of a null space boils down to solving the homogeneous system and isolating the contributions
of free variables. Whether the matrix is in RREF, row echelon form, or not reduced, the null space can be found 
using systematic elimination and back-substitution to express the general solution.

---
