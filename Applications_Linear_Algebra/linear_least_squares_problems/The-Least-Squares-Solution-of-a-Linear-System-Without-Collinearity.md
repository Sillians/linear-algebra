# **The Least-Squares Solution of a Linear System (Without Collinearity)**

---

## **1. Overview**

Given an **inconsistent linear system** $`A\mathbf{x} = \mathbf{b}`$ (no exact solution), we seek the **best approximate solution** that **minimizes the error**.

This is the **least-squares solution**, which projects $`\mathbf{b}`$ onto the **column space** of $`A`$:

$$
\min_{\mathbf{x}} \|\mathbf{b} - A\mathbf{x}\|^2
$$

---

## **2. When Does the Least-Squares Solution Apply?**

* **System is overdetermined**: more equations than unknowns ($`m > n`$)
* **No exact solution exists**: $`\mathbf{b} \notin \text{Col}(A)`$
* **Columns of $`A`$ are linearly independent** (no collinearity)

---

## **3. Geometric Intuition**

* The column space of $`A`$ defines a subspace in $`\mathbb{R}^m`$
* We want the **orthogonal projection** of $`\mathbf{b}`$ onto $`\text{Col}(A)`$
* The error vector $`\mathbf{e} = \mathbf{b} - A\mathbf{x}`$ is **orthogonal** to every column of $A$

---

## **4. Least-Squares Condition**

The optimal solution $`\hat{\mathbf{x}}`$ satisfies:

$$
A^T (A\hat{\mathbf{x}} - \mathbf{b}) = 0
$$

This leads to the **normal equations**:

$$
A^T A \hat{\mathbf{x}} = A^T \mathbf{b}
$$

Provided $`A^T A`$ is invertible, the solution is:

$$
\hat{\mathbf{x}} = (A^T A)^{-1} A^T \mathbf{b}
$$

---

## **5. Finding the Least-Squares Solution (Matrix Form)**

### **Given**:

$$
A = \begin{bmatrix} a_{11} & a_{12} \\ a_{21} & a_{22} \\ a_{31} & a_{32} \end{bmatrix}, \quad \mathbf{b} = \begin{bmatrix} b_1 \\ b_2 \\ b_3 \end{bmatrix}
$$

### **Steps**:

1. Compute $`A^T A`$
2. Compute $`A^T \mathbf{b}`$
3. Solve:

$$
\hat{\mathbf{x}} = (A^T A)^{-1} A^T \mathbf{b}
$$

---

## **6. Example**

Let:

$$
A = \begin{bmatrix} 1 & 1 \\ 1 & 2 \\ 1 & 3 \end{bmatrix}, \quad \mathbf{b} = \begin{bmatrix} 1 \\ 2 \\ 2 \end{bmatrix}
$$

Then:

* $`A^T A = \begin{bmatrix} 3 & 6 \\ 6 & 14 \end{bmatrix}`$
* $`A^T \mathbf{b} = \begin{bmatrix} 5 \\ 12 \end{bmatrix}`$
* Solve:

$$
\hat{\mathbf{x}} = (A^T A)^{-1} A^T \mathbf{b}
$$

---

## **7. Finding the Distance Between a Vector and the Subspace of Solutions**

Let:

* $`\hat{\mathbf{b}} = A\hat{\mathbf{x}}`$ (projection of $`\mathbf{b}`$ onto $`\text{Col}(A)`$)
* The **distance** is the norm of the error vector:

$$
\text{dist}(\mathbf{b}, \text{Col}(A)) = \|\mathbf{b} - A\hat{\mathbf{x}}\|
$$

This is the **shortest distance** from $`\mathbf{b}`$ to the subspace spanned by the columns of $A$.

---

##  Summary Table

| **Concept**                   | **Formula / Description**                             |
| ----------------------------- | ----------------------------------------------------- |
| Least-squares objective       | $`\min \|\mathbf{b} - A\mathbf{x}\|^2`$                 |
| Normal equations              | $`A^T A \hat{\mathbf{x}} = A^T \mathbf{b}`$             |
| Least-squares solution        | $`\hat{\mathbf{x}} = (A^T A)^{-1} A^T \mathbf{b}`$      |
| Residual vector               | $`\mathbf{e} = \mathbf{b} - A\hat{\mathbf{x}}`$         |
| Distance to solution subspace | $`\|\mathbf{e}\| = \|\mathbf{b} - A\hat{\mathbf{x}}\|`$ |
| Geometric interpretation      | Projection of $`\mathbf{b}`$ onto $`\text{Col}(A)`$       |

---
