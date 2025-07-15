## **Vectors Over the Complex Numbers**

---

### **1. Introduction to Complex Vectors**

A **complex vector** is a vector whose entries are **complex numbers**, i.e., elements from $`\mathbb{C}`$. 
These vectors live in the space $`\mathbb{C}^n`$, and they extend many familiar properties from real vectors,
but with added structure due to complex conjugation and the complex inner product.

---

### **2. Calculating the Complex Conjugate of a Complex Vector**

Given a vector $`\mathbf{z} = \begin{bmatrix} z_1 \\ z_2 \\ \vdots \\ z_n \end{bmatrix} \in \mathbb{C}^n`$, its **complex conjugate** is:

$`\overline{\mathbf{z}} = \begin{bmatrix} \overline{z_1} \\\overline{z_2} \\\vdots \\\overline{z_n} \end{bmatrix}`$

#### **Example:**

If $`\mathbf{z} = \begin{bmatrix} 1 + 2i \\ -3i \\ 4 \end{bmatrix}`$, then:

$`\overline{\mathbf{z}} = \begin{bmatrix} 1 - 2i \\ 3i \\ 4 \end{bmatrix}`$

---

### **3. Computing Components of the Real and Imaginary Parts of a Complex Vector**

For any $`\mathbf{z} \in \mathbb{C}^n`$, the **real** and **imaginary** parts are:

* **Real Part:**

$`\operatorname{Re}(\mathbf{z}) = \frac{1}{2}(\mathbf{z} + \overline{\mathbf{z}})`$

* **Imaginary Part:**

$`\operatorname{Im}(\mathbf{z}) = \frac{1}{2i}(\mathbf{z} - \overline{\mathbf{z}})`$

#### **Example:**

Let $`\mathbf{z} = \begin{bmatrix} 2 + i \\ -i \end{bmatrix}`$

Then:

* $`\overline{\mathbf{z}} = \begin{bmatrix} 2 - i \\ i \end{bmatrix}`$
* $`\operatorname{Re}(\mathbf{z}) = \frac{1}{2} \begin{bmatrix} (2+i)+(2-i) \\ (-i)+i \end{bmatrix} = \begin{bmatrix} 2 \\ 0 \end{bmatrix}`$
* $`\operatorname{Im}(\mathbf{z}) = \frac{1}{2i} \begin{bmatrix} (2+i)-(2-i) \\ (-i)-i \end{bmatrix} = \begin{bmatrix} 1 \\ -1 \end{bmatrix}`$

---

### **4. Finding the Real or Imaginary Part of a Scalar Given the Conjugate of a Scaled Vector**

Suppose you're given $`\overline{c \mathbf{z}}`$, and want to find the **real or imaginary part** of the **scalar** $`c \in \mathbb{C}`$. 
If $`\mathbf{z} \in \mathbb{C}^n`$ is known, and $`\overline{c \mathbf{z}}`$ is given, use:

$`\overline{c \mathbf{z}} = \overline{c} \cdot \overline{\mathbf{z}} \Rightarrow \text{Use known } \mathbf{z}, \overline{\mathbf{z}} \text{ to isolate } \overline{c}`$

Once $`\overline{c}`$ is found, take:

* $`\operatorname{Re}(c) = \operatorname{Re}(\overline{\overline{c}})`$
* $`\operatorname{Im}(c) = \operatorname{Im}(\overline{\overline{c}})`$

#### **Example:**

Suppose:

* $`\mathbf{z} = \begin{bmatrix} 1 + i \\ 2 \end{bmatrix}`$
* $`\overline{c \mathbf{z}} = \begin{bmatrix} 3 - i \\ 4 \end{bmatrix}`$

Then:

* $`\overline{c} \cdot \overline{\mathbf{z}} = \begin{bmatrix} 3 - i \\ 4 \end{bmatrix}`$
* $`\overline{\mathbf{z}} = \begin{bmatrix} 1 - i \\ 2 \end{bmatrix}`$

Solve for $`\overline{c}`$ using any component:

$`\overline{c}(1 - i) = 3 - i \Rightarrow \overline{c} = \frac{3 - i}{1 - i} = \frac{(3 - i)(1 + i)}{(1 - i)(1 + i)} = \frac{(3 + 3i - i - i^2)}{2} = \frac{(3 + 2i + 1)}{2} = 2 + i`$

So:

$`c = \overline{(2 + i)} = 2 - i \Rightarrow \operatorname{Re}(c) = 2, \quad \operatorname{Im}(c) = -1`$

---

### ✅ **Summary Table**

| Concept                                         | Expression                                                                         |
| ----------------------------------------------- | ---------------------------------------------------------------------------------- |
| Complex conjugate of a vector                   | $`\overline{\mathbf{z}} = [\overline{z_1}, \dots, \overline{z_n}]^\top`$             |
| Real part of vector                             | $`\operatorname{Re}(\mathbf{z}) = \frac{1}{2}(\mathbf{z} + \overline{\mathbf{z}})`$  |
| Imaginary part of vector                        | $`\operatorname{Im}(\mathbf{z}) = \frac{1}{2i}(\mathbf{z} - \overline{\mathbf{z}})`$ |
| Conjugate of a scalar times vector              | $`\overline{c \mathbf{z}} = \overline{c} \cdot \overline{\mathbf{z}}`$               |
| Recover scalar components from vector conjugate | Use component-wise equations to solve for $`\overline{c}`$, then conjugate it        |

---

### **Applications**

* **Quantum mechanics** and **signal processing** use complex vector spaces.


* The inner product of complex vectors requires conjugation:
  $`\langle \mathbf{u}, \mathbf{v} \rangle = \overline{\mathbf{u}}^\top \mathbf{v}`$


* Used in **Fourier analysis**, **PCA for complex signals**, and **complex-valued neural networks**.
