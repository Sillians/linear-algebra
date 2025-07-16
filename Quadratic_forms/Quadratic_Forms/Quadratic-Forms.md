## **Quadratic Forms**

---

## **Definition**

A **quadratic form** in variables $`x_1, x_2, \dots, x_n`$ is a homogeneous degree-2 polynomial:

$$
Q(\mathbf{x}) = \sum_{i=1}^{n} \sum_{j=1}^{n} a_{ij} x_i x_j = \mathbf{x}^\top A \mathbf{x}
$$

Where:

* $`\mathbf{x} \in \mathbb{R}^n`$ is a column vector


* $`A \in \mathbb{R}^{n \times n}`$ is a **symmetric matrix** (i.e. $`A = A^\top`$)


If $A$ is not symmetric, use the **symmetrized form**:

$$
Q(\mathbf{x}) = \mathbf{x}^\top \left( \frac{A + A^\top}{2} \right) \mathbf{x}
$$

---

## **1. Identifying Matrices of Quadratic Forms**

Given a quadratic form:

$$
Q(x) = \sum_{i=1}^n a_{ii} x_i^2 + \sum_{1 \le i < j \le n} a_{ij} x_i x_j
$$

Construct matrix $`A`$ as:

* $`A_{ii} =`$ coefficient of $`x_i^2`$


* $`A_{ij} = A_{ji} = \frac{1}{2} \times`$ coefficient of $`x_i x_j`$


### **Example**

Given:

$$
Q(x) = 2x_1^2 + 4x_1x_2 + 3x_2^2
$$

Then:

$$
A = \begin{bmatrix}
2 & 2 \\
2 & 3
\end{bmatrix}
$$

---

## **2. Evaluating a Quadratic Form**

To compute $`Q(\mathbf{x}) = \mathbf{x}^\top A \mathbf{x}`$:

1. Multiply $`A\mathbf{x}`$


2. Multiply $`\mathbf{x}^\top`$ with the result


### **Example**

Let

$$
A = \begin{bmatrix} 1 & 2 \\ 2 & 4 \end{bmatrix}, \quad \mathbf{x} = \begin{bmatrix} 3 \\ 1 \end{bmatrix}
$$

Then:

$$
Q(\mathbf{x}) = \mathbf{x}^\top A \mathbf{x} = 
[3 \quad 1]
\begin{bmatrix} 1 & 2 \\ 2 & 4 \end{bmatrix}
\begin{bmatrix} 3 \\ 1 \end{bmatrix} = 25
$$

---

## **3. Writing Down a Quadratic Form Given Its Matrix**

Given a symmetric matrix $`A`$, the quadratic form is:

$$
Q(x) = \sum_{i=1}^n A_{ii} x_i^2 + \sum_{1 \le i < j \le n} 2A_{ij} x_i x_j
$$

### **Example**

Given:

$$
A = \begin{bmatrix}
1 & -2 & 0 \\
-2 & 3 & 4 \\
0 & 4 & 5
\end{bmatrix}
$$

Then:

$$
Q(x) = 1x_1^2 + 3x_2^2 + 5x_3^2 - 4x_1x_2 + 8x_2x_3
$$

---

## **4. Finding the Matrix of a Quadratic Form**

From a given quadratic form, build matrix $`A`$ as:

* For each $`x_i^2`$, place its coefficient in $`A_{ii}`$


* For each $`x_i x_j`$ with $`i \ne j`$, place half the coefficient in both $`A_{ij}`$ and $`A_{ji}`$


### **Example**

Given:

$$
Q(x) = 2x_1^2 + 6x_1x_2 - 4x_2^2 + 8x_2x_3
$$

Then:

$$
A = \begin{bmatrix}
2 & 3 & 0 \\
3 & -4 & 4 \\
0 & 4 & 0
\end{bmatrix}
$$

---

## **Key Properties**

* **Symmetric matrix**: All quadratic forms use symmetric matrices.

* **Definiteness**:

* Positive definite ⇔ $`\mathbf{x}^\top A \mathbf{x} > 0`$ for all $`\mathbf{x} \ne 0`$
* Negative definite ⇔ $`\mathbf{x}^\top A \mathbf{x} < 0`$ for all $`\mathbf{x} \ne 0`$
* Indefinite ⇔ takes both positive and negative values


* **Diagonalization**: There exists orthogonal matrix $P$ such that:

$$
Q(\mathbf{x}) = \mathbf{x}^\top A \mathbf{x} = \mathbf{y}^\top D \mathbf{y}
$$

Where:

* $`D = P^\top A P`$ is diagonal


* $`\mathbf{y} = P^\top \mathbf{x}`$

---

## **Quick Reference Table**

| Quadratic Form Term           | Corresponding Entry in $`A`$                         |
|-------------------------------| -------------------------------------------------- |
| $`x_i^2`$                     | $`A_{ii}`$                                           |
| $`x_i x_j`$ (for $`i \ne j`$) | $`A_{ij} = A_{ji} = \frac{1}{2} \times`$ coefficient |
| Given $`A`$, write $`Q(x)`$   | Use $`A_{ii} x_i^2$ and $2A_{ij} x_i x_j`$ terms     |


