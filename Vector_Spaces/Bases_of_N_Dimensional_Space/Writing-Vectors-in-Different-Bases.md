## **Writing Vectors in Different Bases**

Understanding how to express vectors in different bases is a foundational concept in linear algebra, especially useful in applications like machine learning, computer graphics, and systems theory.

---

### **1. Overview**

Given a vector space and a basis $`\mathcal{B} = \{ \mathbf{b}_1, \mathbf{b}_2, \dots, \mathbf{b}_n \}`$, any vector $`\mathbf{x}`$ in the space can be expressed uniquely as:

$$
\mathbf{x} = c_1 \mathbf{b}_1 + c_2 \mathbf{b}_2 + \dots + c_n \mathbf{b}_n
$$

The scalars $`c_1, c_2, \dots, c_n`$ are called the **coordinates of $`\mathbf{x}`$ relative to the basis $`\mathcal{B}`$**.

---

### **2. Writing a Two-Dimensional Vector in a Different Basis**

Let:

$`\mathbf{x} = \begin{pmatrix} 4 \\ 3 \end{pmatrix}, \quad \mathcal{B} = \left\{ \begin{pmatrix} 1 \\ 0 \end{pmatrix}, \begin{pmatrix} 0 \\ 1 \end{pmatrix} \right\}`$

This is the standard basis. Then:


$`[\mathbf{x}]_{\mathcal{B}} = \begin{pmatrix} 4 \\ 3 \end{pmatrix}`$


Now consider a different basis:


$`\mathcal{B}' = \left\{ \begin{pmatrix} 1 \\ 1 \end{pmatrix}, \begin{pmatrix} 1 \\ -1 \end{pmatrix} \right\}`$


To find $`[\mathbf{x}]_{\mathcal{B}'}`$, solve:


$`\mathbf{x} = a \begin{pmatrix} 1 \\ 1 \end{pmatrix} + b \begin{pmatrix} 1 \\ -1 \end{pmatrix} \Rightarrow \begin{pmatrix} 4 \\ 3 \end{pmatrix} = a \begin{pmatrix} 1 \\ 1 \end{pmatrix} + b \begin{pmatrix} 1 \\ -1 \end{pmatrix}`$



$`\Rightarrow \begin{cases} a + b = 4 \\a - b = 3 \end{cases} \Rightarrow a = \frac{7}{2}, \quad b = \frac{1}{2}`$

$`[\mathbf{x}]_{\mathcal{B}'} = \begin{pmatrix} \frac{7}{2} \\ \frac{1}{2} \end{pmatrix}`$

---

### **3. Writing a Three-Dimensional Vector in a Different Basis**

Let:

$`\mathbf{x} = \begin{pmatrix} 1 \\ 4 \\ 3 \end{pmatrix}`$


and


$`\mathcal{B} = \left\{ \begin{pmatrix} 1 \\ 0 \\ 0 \end{pmatrix}, \begin{pmatrix} 0 \\ 1 \\ 1 \end{pmatrix}, \begin{pmatrix} 0 \\ 1 \\ -1 \end{pmatrix} \right\}`$


We want to solve:


$`\mathbf{x} = a \mathbf{b}_1 + b \mathbf{b}_2 + c \mathbf{b}_3`$


Write matrix $A$ from the basis vectors:


$`A = \begin{pmatrix} 1 & 0 & 0 \\0 & 1 & 1 \\0 & 1 & -1 \end{pmatrix}`$


Then compute:


$`[\mathbf{x}]_{\mathcal{B}} = A^{-1} \mathbf{x}`$

(You can compute the inverse or solve the linear system $`A\mathbf{v} = \mathbf{x}`$ for the coordinates.)

---

### **4. Writing a Vector in a Different Basis Given a Linear Relationship Between Two Bases**

Suppose:


$`\mathbf{x}_{\mathcal{C}} = \begin{pmatrix} 2 \\ -1 \end{pmatrix}, \quad \text{and} \quad \mathcal{C} = \{ \mathbf{c}_1, \mathbf{c}_2 \}`$


Let $`\mathcal{C}`$ and $`\mathcal{B}`$ be related by:


$`\mathbf{c}_i = T \mathbf{b}_i \quad \text{for a change of basis matrix } T`$


Then:


$`[\mathbf{x}]_{\mathcal{B}} = T^{-1} [\mathbf{x}]_{\mathcal{C}}`$


In general, **to convert coordinates from one basis to another**, use:


$`[\mathbf{x}]_{\mathcal{B}} = P^{-1} [\mathbf{x}]_{\mathcal{S}}, \quad \text{where } P = [\mathbf{b}_1 \ \mathbf{b}_2 \ \dots \ \mathbf{b}_n]`$

---

### **Summary Table**

| Operation                                        | Formula / Description                                            |
| ------------------------------------------------ | ---------------------------------------------------------------- |
| Expressing vector in standard basis              | $`\mathbf{x} = c_1 \mathbf{e}_1 + c_2 \mathbf{e}_2 + \dots`$      |
| Changing basis (matrix form)                     | $`[\mathbf{x}]_{\mathcal{B}} = A^{-1} \mathbf{x}`$                |
| Reconstructing vector from coordinates and basis | $`\mathbf{x} = A [\mathbf{x}]_{\mathcal{B}}`$                     |
| Basis change via transformation matrix           | $`[\mathbf{x}]_{\mathcal{B}} = T^{-1} [\mathbf{x}]_{\mathcal{C}}`$ |
| Coordinates from vector (solve linear system)    | $`A \mathbf{v} = \mathbf{x}`$                                      |

---

This framework allows accurate conversion between coordinate systems defined by various bases, critical in many mathematical and computational applications.
