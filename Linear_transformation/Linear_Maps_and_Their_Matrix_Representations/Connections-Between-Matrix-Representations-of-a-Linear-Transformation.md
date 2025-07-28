## **Connections Between Matrix Representations of a Linear Transformation**

---

### **1. Overview**

A **linear transformation** $`T: V \to V`$ can be represented in different matrix forms depending on the **choice of basis**. 

These representations are **connected** by change-of-coordinates (change-of-basis) matrices.


* If we change the basis of the space $`V`$, the matrix representation of $`T`$ changes.


* However, the **action of the transformation** remains the same.


* These matrix representations are related via **similarity transformations**.

---

### **2. Identifying Connections Between Matrices of a Linear Transformation Relative to Different Bases**

Let:

* $`T: V \to V`$ be a linear transformation.


* $`\mathcal{B} = \{ \mathbf{v}_1, \dots, \mathbf{v}_n \}`$, $`\mathcal{B}' = \{ \mathbf{v}_1', \dots, \mathbf{v}_n' \}`$ be two bases of $V$.


* $`[T]_{\mathcal{B}}`$ and $`[T]_{\mathcal{B}'}`$ be the matrices of $`T`$ with respect to $`\mathcal{B}`$ and $`\mathcal{B}'`$, respectively.


* $`P`$ be the **change-of-coordinates matrix** from $`\mathcal{B}'`$ to $`\mathcal{B}`$:

  $`[\mathbf{x}]_{\mathcal{B}} = P [\mathbf{x}]_{\mathcal{B}'}`$

Then, the **connection** between the two matrix representations is:


$`[T]_{\mathcal{B}'} = P^{-1} [T]_{\mathcal{B}} P`$


This is known as a **similarity transformation**.

---

### **3. Finding the Matrix of a Linear Transformation Relative to a Basis Using a Change-of-Coordinates Matrix**

Suppose:

* $`[T]_{\mathcal{B}}`$ is known.


* $`\mathcal{B}`$ is a basis of $`V`$.


* $`\mathcal{E}`$ is the standard basis.


* $`P`$ is the change-of-coordinates matrix from $`\mathcal{B}`$ to $`\mathcal{E}`$:


  Columns of $`P`$ are the vectors of $`\mathcal{B}`$ expressed in the standard basis.


To compute the matrix of $T$ **in the standard basis** $`[T]_{\mathcal{E}}`$:


$`[T]_{\mathcal{E}} = P [T]_{\mathcal{B}} P^{-1}`$


To compute $`[T]_{\mathcal{B}}`$ from $`[T]_{\mathcal{E}}`$:


$`[T]_{\mathcal{B}} = P^{-1} [T]_{\mathcal{E}} P`$

This reverses the change of basis.

---

### **4. Finding the Matrix of a Linear Transformation Relative to the Standard Basis**

To find the matrix of $`T`$ relative to the **standard basis**:

1. Apply $`T`$ to each standard basis vector $`\mathbf{e}_1, \dots, \mathbf{e}_n`$.


2. Write each result $`T(\mathbf{e}_i)`$ as a column vector.


3. Form the matrix:

$`[T]_{\text{std}} = \begin{bmatrix} T(\mathbf{e}_1) & T(\mathbf{e}_2) & \dots & T(\mathbf{e}_n)\end{bmatrix}`$


Each column is the image of a standard basis vector under $`T`$, written in standard coordinates.

---

### **5. Finding the Matrix of a Linear Transformation Relative to a Given Basis**

Let:

* $`\mathcal{B} = \{ \mathbf{v}_1, \dots, \mathbf{v}_n \}`$


* $`T: V \to V`$


Steps:

1. Apply $T$ to each $`\mathbf{v}_i`$:
   Compute $`T(\mathbf{v}_1), \dots, T(\mathbf{v}_n)`$


2. Express each $`T(\mathbf{v}_i)`$ **as a linear combination** of $`\mathcal{B}`$:


$`T(\mathbf{v}_i) = a_{1i} \mathbf{v}_1 + \dots + a_{ni} \mathbf{v}_n`$


3. The matrix $`[T]_{\mathcal{B}}`$ has columns:


$`[T]_{\mathcal{B}} = \begin{bmatrix}[T(\mathbf{v}_1)]_{\mathcal{B}} & \dots & [T(\mathbf{v}_n)]_{\mathcal{B}} \end{bmatrix}`$


This matrix captures the transformation’s action entirely within the chosen basis $`\mathcal{B}`$.

---

### **Summary Table**

| **Objective**                                                        | **Approach / Formula**                              |
|----------------------------------------------------------------------|-----------------------------------------------------|
| Connect two matrices relative to bases $`\mathcal{B}, \mathcal{B}'`$ | $`[T]_{\mathcal{B}'} = P^{-1} [T]_{\mathcal{B}} P`$ |
| Matrix in standard basis from basis $`\mathcal{B}`$                  | $`[T]_{\text{std}} = P [T]_{\mathcal{B}} P^{-1}`$   |
| Matrix in basis $`\mathcal{B}`$ from standard basis                  | $`[T]_{\mathcal{B}} = P^{-1} [T]_{\text{std}} P`$   |
| Find matrix relative to standard basis                               | Use $`T(\mathbf{e}_i)`$ as columns                  |
| Find matrix relative to basis $`\mathcal{B}`$                        | Columns are $`[T(\mathbf{v}_i)]_{\mathcal{B}}`$     |

---