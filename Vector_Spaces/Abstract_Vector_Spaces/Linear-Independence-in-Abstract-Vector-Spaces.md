## **Linear Independence in Abstract Vector Spaces**

---

### **1. What Is Linear Independence?**

In a vector space $V$, a set of vectors $`\{v_1, v_2, \dots, v_k\} \subseteq V`$ is said to be **linearly independent** if the **only** solution to the equation:

$`c_1 v_1 + c_2 v_2 + \dots + c_k v_k = 0`$

is:

$`c_1 = c_2 = \dots = c_k = 0`$

Otherwise, the set is **linearly dependent** — meaning at least one vector is a linear combination of the others.

This concept generalizes to **abstract vector spaces**, such as:

* Spaces of polynomials $`\mathbb{P}_n`$
* Spaces of matrices $`\mathbb{R}^{m \times n}`$
* Function spaces

---

### **2. Finding the Coefficients That Show Linear Dependence Among Polynomial Vectors**

Consider polynomials:

$`p_1(x) = 1 + x, \quad p_2(x) = x + x^2, \quad p_3(x) = 1 + x^2`$

To test linear dependence, form:

$`c_1 p_1(x) + c_2 p_2(x) + c_3 p_3(x) = 0`$

This gives:

$`c_1(1 + x) + c_2(x + x^2) + c_3(1 + x^2) = 0 \Rightarrow (c_1 + c_3) + (c_1 + c_2)x + (c_2 + c_3)x^2 = 0`$

Set coefficients to zero:

$`\begin{cases} c_1 + c_3 = 0 \\c_1 + c_2 = 0 \\c_2 + c_3 = 0 \end{cases} \Rightarrow \text{Nontrivial solution: linearly dependent}`$

---

### **3. Finding the Coefficients That Show Linear Dependence Among Matrix Vectors**

Let:

$`A_1 = \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix}, \quad A_2 = \begin{bmatrix} 2 & 1 \\ 0 & 1 \end{bmatrix}, \quad A_3 = \begin{bmatrix} -1 & -1 \\ 0 & -1 \end{bmatrix}`$


We ask: are these matrices linearly dependent?

Set:

$`c_1 A_1 + c_2 A_2 + c_3 A_3 = 0_{2 \times 2}`$

Compute each entry:

$`c_1 \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix} + c_2 \begin{bmatrix} 2 & 1 \\ 0 & 1 \end{bmatrix} + c_3 \begin{bmatrix} -1 & -1 \\ 0 & -1 \end{bmatrix} = \begin{bmatrix} 0 & 0 \\ 0 & 0 \end{bmatrix}`$

Which leads to:

$`\begin{cases} c_1 + 2c_2 - c_3 = 0 \\c_2 - c_3 = 0 \\c_1 + c_2 - c_3 = 0 \end{cases} \Rightarrow \text{System has nontrivial solution} \Rightarrow \text{Linearly dependent}`$

---

### **4. Determining if a Given Set Is Linearly Independent Given Information on Its Elements**

#### **Example 1:**

Given $`v_1, v_2, v_3 \in V`$ such that:

$`2v_1 - v_2 + 3v_3 = 0`$

This directly shows **linear dependence**, since nonzero coefficients exist such that the linear combination is 0.

#### **Example 2:**

Suppose $`\{f_1, f_2\} \subset \mathcal{F}`$, a function space, and:

$`f_1(x) = \sin(x), \quad f_2(x) = \cos(x)`$

We know $`\sin(x)`$ and $`\cos(x)`$ are not scalar multiples of each other over $`\mathbb{R}`$, so the set is **linearly independent**.

---

### ✅ **Summary Table**

| Concept             | Description                                                          |
| ------------------- | -------------------------------------------------------------------- |
| Linear independence | $`c_1 v_1 + \dots + c_k v_k = 0 \Rightarrow c_1 = \dots = c_k = 0`$    |
| Linear dependence   | There exist nonzero scalars $`c_i`$ such that the combination equals 0 |
| Polynomials         | Compare coefficients of like powers to test dependence               |
| Matrices            | Combine entries as systems of equations                              |
| Function spaces     | Use pointwise evaluation or known independence results               |

---

### **Applications**

* Basis construction
* Determining spanning sets
* Dimension of vector spaces
* Understanding redundancy in data or function approximations
