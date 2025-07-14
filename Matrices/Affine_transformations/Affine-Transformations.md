## **Affine Transformations**

An **affine transformation** is a geometric transformation that preserves **points, 
straight lines**, and **planes**. It combines **linear transformations** 
(like rotations, scalings, shears) with **translations**. Affine transformations 
are foundational in computer graphics, robotics, and machine learning (e.g., neural network layers).

---

### **1. Identifying Affine Transformations**

An affine transformation $`T: \mathbb{R}^n \to \mathbb{R}^n`$ can be written in the general form:

$$
\boxed{T(\mathbf{x}) = A\mathbf{x} + \mathbf{b}}
$$

Where:

* $`\mathbf{x}`$ is a vector in $`\mathbb{R}^n`$


* $`A`$ is an $`n \times n`$ matrix (linear transformation)


* $`\mathbf{b} \in \mathbb{R}^n`$ is a translation vector



This form defines **affine maps** because they preserve:

* Parallelism (but not necessarily lengths or angles)


* Convex combinations (affine combinations of points)

---

### **2. Finding the Parametric Representation of an Affine Transformation Given Its Matrix Form**

Given the **matrix form**:

$$
T(\mathbf{x}) = A\mathbf{x} + \mathbf{b}
$$

You can write the **parametric representation** explicitly by expanding the transformation in 
terms of the input coordinates.

#### **Example (2D):**

Let:

$$
A = \begin{bmatrix} 2 & 0 \\ 1 & 3 \end{bmatrix}, \quad \mathbf{b} = \begin{bmatrix} 1 \\ -2 \end{bmatrix}
$$

Then:

$$
T(x, y) = A \begin{bmatrix} x \\ y \end{bmatrix} + \mathbf{b}
= \begin{bmatrix} 2x \\ x + 3y \end{bmatrix} + \begin{bmatrix} 1 \\ -2 \end{bmatrix}
= \begin{bmatrix} 2x + 1 \\ x + 3y - 2 \end{bmatrix}
$$

This is the **parametric representation**:

$$
T(x, y) = (2x + 1,\ x + 3y - 2)
$$

---

### **3. Finding the Matrix Representation of an Affine Transformation Given Its Parametric Form**

To reverse the process, extract the **matrix $A$** and **vector $\mathbf{b}$** from the given parametric form.

#### **Example:**

Given:

$$
T(x, y) = (4x + 2y + 1,\ -x + 3y - 5)
$$

Identify linear and constant terms:

* First component: $`4x + 2y + 1`$


* Second component: $`-x + 3y - 5`$


So:

* Matrix $`A = \begin{bmatrix} 4 & 2 \\ -1 & 3 \end{bmatrix}`$


* Translation vector $`\mathbf{b} = \begin{bmatrix} 1 \\ -5 \end{bmatrix}`$

Therefore:

$`T(\mathbf{x}) = A\mathbf{x} + \mathbf{b}  = \begin{bmatrix} 4 & 2 \\ -1 & 3 \end{bmatrix} \begin{bmatrix} x \\ y \end{bmatrix} + \begin{bmatrix} 1 \\ -5 \end{bmatrix} `$

---

### ✅ **Summary Table**

| Task                               | Description                                                        |
| ---------------------------------- | ------------------------------------------------------------------ |
| **Identify affine transformation** | $`T(\mathbf{x}) = A\mathbf{x} + \mathbf{b}`$                         |
| **From matrix to parametric**      | Multiply $`A\mathbf{x}`$, add $`\mathbf{b}`$                           |
| **From parametric to matrix**      | Extract coefficients → matrix $`A`$; constants → vector $`\mathbf{b}`$ |
| **Preserved properties**           | Parallel lines, affine combinations, straightness                  |

---

### **Conclusion**

Affine transformations unify linear transformations and translations in a single model, 
forming the basis of transformations in geometry, graphics, and optimization. 
Understanding how to convert between matrix and parametric forms enables deeper 
insights into spatial reasoning, especially in applied mathematics and engineering contexts.
