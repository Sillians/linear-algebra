## **Quadratic Forms: Positive-Definite and Negative-Definite**

---

### **1. Overview of Quadratic Forms**

A **quadratic form** in $`n`$ variables is defined as:

$$
Q(\mathbf{x}) = \mathbf{x}^T A \mathbf{x}
$$

where:

* $`\mathbf{x} \in \mathbb{R}^n`$ is a column vector,
* $`A \in \mathbb{R}^{n \times n}`$ is a **symmetric matrix** ($`A = A^T`$),
* $`Q(\mathbf{x})`$ is a scalar value.

---

### **2. Types of Quadratic Forms**

| Type                  | Definition                               | Sign of $`Q(\mathbf{x})`$ for $`\mathbf{x} \neq 0`$ |
| --------------------- | ---------------------------------------- |----------------------------------------------------|
| Positive-definite     | $`Q(\mathbf{x}) > 0`$                     | Always positive                                    |
| Negative-definite     | $`Q(\mathbf{x}) < 0`$                     | Always negative                                    |
| Positive-semidefinite | $`Q(\mathbf{x}) \geq 0`$                  | Non-negative                                       |
| Negative-semidefinite | $`Q(\mathbf{x}) \leq 0`$                  | Non-positive                                       |
| Indefinite            | $`Q(\mathbf{x})`$ can be both $`>`$ and $`<`$ 0 | Mixed signs                                        |

---

### **3. Identifying Quadratic Form Type**

---

#### **A. Using Substitution**

Steps:

1. Choose a few nonzero vectors $`\mathbf{x}`$.
2. Evaluate $`Q(\mathbf{x}) = \mathbf{x}^T A \mathbf{x}`$.

**Example**:
Let

$$
A = \begin{bmatrix} 1 & 0 \\ 0 & -1 \end{bmatrix}
$$

Then:

* $`Q\left(\begin{bmatrix} 1 \ 0 \end{bmatrix}\right) = 1`$
* $`Q\left(\begin{bmatrix} 0 \ 1 \end{bmatrix}\right) = -1`$

**Conclusion**: Since both positive and negative values occur, the form is **indefinite**.

> ⚠️ Substitution can demonstrate indefiniteness, but **cannot confirm** definiteness (since it tests only a few vectors).

---

#### **B. Using Eigenvalues of $A$**

A real symmetric matrix $`A`$ is diagonalizable and has **real eigenvalues**.

##### **Definiteness Criteria:**

| Eigenvalues of $`A`$        | Type                  |
|-----------------------------| --------------------- |
| All $`> 0`$                 | Positive-definite     |
| All $`< 0`$                 | Negative-definite     |
| All $`\geq 0`$              | Positive-semidefinite |
| All $`\leq 0`$              | Negative-semidefinite |
| Mixed (positive & negative) | Indefinite            |

**Example**:

$$
A = \begin{bmatrix} 2 & -1 \\ -1 & 2 \end{bmatrix}
$$

Eigenvalues: $`\lambda\_1 = 1`$, $`\lambda\_2 = 3`$

$`\Rightarrow`$ **Positive-definite**

---

#### **C. Using Sylvester's Criterion**

Check the **leading principal minors** of the symmetric matrix $`A`$.

* $`A`$ is **positive-definite** ⟺ all leading principal minors are **positive**.
* $`A`$ is **negative-definite** ⟺ minors alternate in sign as $`(-1)^k \cdot \text{minor}\_k > 0`$.

**Example**:

$$
A = \begin{bmatrix} 2 & -1 \\ -1 & 2 \end{bmatrix}
$$

* 1st leading minor: $`2 > 0`$
* 2nd leading minor (determinant): $`\det(A) = 4 - 1 = 3 > 0`$

✅ All leading minors are positive $`\Rightarrow`$ **Positive-definite**

---

### **4. Summary Table**

| Method                | Description                              | Best For                       |
| --------------------- | ---------------------------------------- | ------------------------------ |
| Substitution          | Test $`Q(\mathbf{x})`$ on selected vectors | Detecting **indefiniteness**   |
| Eigenvalues           | Check signs of eigenvalues of $`A`$       | All form types                 |
| Sylvester’s Criterion | Evaluate leading principal minors of $`A`$ | Positive/Negative-definiteness |

---

### **5. Final Notes**

* Always ensure the matrix $`A`$ is **symmetric** before applying tests.
* Use **eigenvalues** or **Sylvester’s Criterion** for definitive classification.
* For large matrices, eigenvalue analysis is more efficient via numerical tools.

---
