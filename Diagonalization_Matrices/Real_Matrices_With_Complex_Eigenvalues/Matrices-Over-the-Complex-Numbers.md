## **Matrices Over the Complex Numbers**

Matrices with complex entries extend the familiar rules of linear algebra into the complex plane. 
These matrices are essential in quantum mechanics, signal processing, control theory, and many advanced fields of mathematics.

---

### **1. Complex Matrix Basics**

A **complex matrix** is a matrix whose entries are complex numbers of the form:

$`z = a + bi \quad \text{where } a, b \in \mathbb{R},\ i = \sqrt{-1}`$

The set of all $`m \times n`$ matrices with complex entries is denoted by $`M\_{m \times n}(\mathbb{C})`$.

---

### **2. Calculating the Complex Conjugate of a Complex Matrix**

**Definition:**
The **complex conjugate** of a complex matrix $`A = [a\_{ij}]`$ is denoted by $`\overline{A}`$ and defined elementwise:

$`\overline{A} = [\overline{a_{ij}}]`$

where $`\overline{a\_{ij}}`$ is the complex conjugate of $`a\_{ij}`$.


**Example:**
Let

$`A = \begin{bmatrix} 1 + 2i & 3 - i \\-2i & 4 \end{bmatrix}`$

Then

$`\overline{A} = \begin{bmatrix} 1 - 2i & 3 + i \\2i & 4 \end{bmatrix}`$

---

### **3. Real and Imaginary Parts of a Complex Matrix**

Any complex matrix $`A`$ can be written as:

$`A = \mathrm{Re}(A) + i\,\mathrm{Im}(A)`$

Where:

* $`\mathrm{Re}(A)`$ is the **real part**, obtained by taking the real part of each entry.


* $`\mathrm{Im}(A)`$ is the **imaginary part**, obtained by taking the imaginary part of each entry.


**Example:**
Let

$`A = \begin{bmatrix} 2 + 3i & -i \\4 & 5i \end{bmatrix}`$

Then

$`\mathrm{Re}(A) = \begin{bmatrix} 2 & 0 \\4 & 0 \end{bmatrix}, \quad \mathrm{Im}(A) = \begin{bmatrix} 3 & -1 \\0 & 5 \end{bmatrix}`$

---

### **4. Multiplying Complex Matrices**

Matrix multiplication over complex numbers follows the same rule as for real matrices, but uses complex arithmetic.

**If** $`A \in M\_{m \times n}(\mathbb{C})`$, $`B \in M\_{n \times p}(\mathbb{C})`$,

then the product $`C = AB \in M\_{m \times p}(\mathbb{C})`$ has entries:


$``c_{ij} = \sum_{k=1}^{n} a_{ik} b_{kj}`$

**Example:**
Let

$`A = \begin{bmatrix} 1 + i & 2 \\0 & 3 - i \end{bmatrix}, \quad B = \begin{bmatrix} 1 & i \\2i & 1 \end{bmatrix}`$

Then

$`AB = \begin{bmatrix} (1 + i)(1) + 2(2i) & (1 + i)(i) + 2(1) \\ 0(1) + (3 - i)(2i) & 0(i) + (3 - i)(1) \end{bmatrix} = \begin{bmatrix} 1 + i + 4i & i + i^2 + 2 \\ 6i - 2 & 3 - i \end{bmatrix} = \begin{bmatrix} 1 + 5i & 1 + i \\6i - 2 & 3 - i \end{bmatrix}`$

---

### **5. Applying Row Operations to a Complex Matrix**

The **elementary row operations** still apply to complex matrices:

1. **Row swapping:** $`R\_i \leftrightarrow R\_j`$


2. **Scalar multiplication:** $`R\_i \rightarrow \lambda R\_i`$ for $`\lambda \in \mathbb{C} \setminus {0}`$


3. **Row addition:** $`R\_i \rightarrow R\_i + \lambda R\_j`$ for $`\lambda \in \mathbb{C}`$



These operations are used in Gaussian elimination over $`\mathbb{C}`$ for solving systems or computing rank.

**Example:**

Given

$`A = \begin{bmatrix} 1 + i & 2 \\i & 1 \end{bmatrix}`$

To eliminate the lower-left entry using $`R\_2 \rightarrow R\_2 - \frac{i}{1 + i} R\_1`$

Simplify the scalar:

$`\frac{i}{1 + i} = \frac{i(1 - i)}{(1 + i)(1 - i)} = \frac{i - i^2}{1 + 1} = \frac{i + 1}{2}`$

Then

$`R_2 = \begin{bmatrix} i & 1 \end{bmatrix} - \frac{1 + i}{2} \begin{bmatrix} 1 + i & 2 \end{bmatrix}`$

Carry out the subtraction and simplify entry-wise.

---

### **Summary Table**

| Operation                          | Description                                        |
|------------------------------------|----------------------------------------------------|
| Complex Conjugate $`\overline{A}`$ | Take conjugate of each entry                       |
| $`\mathrm{Re}(A), \mathrm{Im}(A)`$ | Real and imaginary component matrices              |
| Matrix Multiplication              | Same rule as reals, using complex arithmetic       |
| Row Operations                     | Performed over $`\mathbb{C}`$ with complex scalars |

---
