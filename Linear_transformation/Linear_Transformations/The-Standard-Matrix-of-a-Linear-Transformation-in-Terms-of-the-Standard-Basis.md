## **The Standard Matrix of a Linear Transformation in Terms of the Standard Basis**

---

### **I. Overview: Linear Transformations and Standard Matrices**

A **linear transformation** $`T: \mathbb{R}^n \to \mathbb{R}^m`$ maps vectors in one space to another while preserving vector addition and scalar multiplication:


* $`T(\mathbf{u} + \mathbf{v}) = T(\mathbf{u}) + T(\mathbf{v})`$


* $`T(c\mathbf{v}) = cT(\mathbf{v})`$

Each such transformation is associated with a unique **standard matrix** $`A`$ such that:


$`T(\mathbf{x}) = A\mathbf{x}`$

---

### **II. Constructing the Standard Matrix**

Given a linear transformation $`T: \mathbb{R}^n \to \mathbb{R}^m`$, let $`\{ \mathbf{e}_1, \mathbf{e}_2, \dots, \mathbf{e}_n \}`$ be the standard basis 
of $`\mathbb{R}^n`$. The standard matrix $`A`$ is constructed by:


$`A = \begin{bmatrix} T(\mathbf{e}_1) & T(\mathbf{e}_2) & \dots & T(\mathbf{e}_n) \end{bmatrix}`$


Each column of $`A`$ is the image of a standard basis vector under $`T`$.

---

### **III. Determining the Standard Matrix Given the Image of the Standard Basis**

If you're told:

* $`T(\mathbf{e}_1) = \mathbf{v}_1`$


* $`T(\mathbf{e}_2) = \mathbf{v}_2`$


* $`\dots`$


* $`T(\mathbf{e}_n) = \mathbf{v}_n`$

Then:


$`A = \begin{bmatrix} \mathbf{v}_1 & \mathbf{v}_2 & \dots & \mathbf{v}_n \end{bmatrix}`$


This gives a direct column-wise construction of the matrix representing $`T`$.

---

### **IV. Determining the Standard Matrix Given a Diagram**

A diagram may visually display the images of basis vectors. Suppose arrows or mappings show:

* $`\mathbf{e}_1 \mapsto \begin{bmatrix} a \\ b \end{bmatrix}`$


* $`\mathbf{e}_2 \mapsto \begin{bmatrix} c \\ d \end{bmatrix}`$

Then the standard matrix of $`T: \mathbb{R}^2 \to \mathbb{R}^2`$ is:


$`A = \begin{bmatrix} a & c \\b & d \end{bmatrix}`$


You can always build the matrix by reading how the basis vectors are mapped in the diagram.

---

### **V. Determining the Images of the Standard Basis Vectors Under a Given Linear Transformation**

Suppose you are given the transformation in matrix form:

* $`A = \begin{bmatrix} a_{11} & a_{12} \\ a_{21} & a_{22} \end{bmatrix}`$

Then:

* $`T(\mathbf{e}_1) = A \mathbf{e}_1 = \begin{bmatrix} a_{11} \\ a_{21} \end{bmatrix}`$


* $`T(\mathbf{e}_2) = A \mathbf{e}_2 = \begin{bmatrix} a_{12} \\ a_{22} \end{bmatrix}`$


The image of each basis vector is the corresponding column of $A$.

---

### **VI. Summary Table**

| **Input**                         | **Operation**                            | **Result**                                       |
|-----------------------------------|------------------------------------------|--------------------------------------------------|
| Images of standard basis vectors  | Stack as columns                         | Get standard matrix $`A`$                        |
| Diagram with mapped arrows        | Read terminal points of $`\mathbf{e}_i`$ | Form matrix columns                              |
| Given matrix $`A`$                | Multiply with $`\mathbf{e}_i`$           | Get $`T(\mathbf{e}_i)`$ as column $`i`$ of $`A`$ |

---

