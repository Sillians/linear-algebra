## **The Matrix of a Linear Map Relative to Two Bases**

---

### **1. Overview**

A **linear map** $`T: V \to W`$ between finite-dimensional vector spaces can be represented by a matrix once **bases** for $V$ and $W$ are fixed. 
This matrix allows us to translate between abstract vector operations and concrete matrix computations.


* **Domain basis** $`\mathcal{B} = \{ \mathbf{v}_1, \dots, \mathbf{v}_n \} \subseteq V`$


* **Codomain basis** $`\mathcal{C} = \{ \mathbf{w}_1, \dots, \mathbf{w}_m \} \subseteq W`$


The matrix **$`[T]_{\mathcal{C} \leftarrow \mathcal{B}}`$** is the **matrix of the linear transformation $`T`$** relative to domain basis $`\mathcal{B}`$ and codomain basis $`\mathcal{C}`$.

---

### **2. Finding the Matrix of a Linear Map Relative to Two Bases Using the Definition**

To compute the matrix $`[T]_{\mathcal{C} \leftarrow \mathcal{B}}`$:

1. **Apply** the linear map $T$ to each vector in $`\mathcal{B}`$:


$`T(\mathbf{v}_1), T(\mathbf{v}_2), \dots, T(\mathbf{v}_n)`$


2. **Express** each $`T(\mathbf{v}_j)`$ as a linear combination of the vectors in $`\mathcal{C}`$:


$`T(\mathbf{v}_j) = a_{1j} \mathbf{w}_1 + \dots + a_{mj} \mathbf{w}_m`$


3. The **matrix $`[T]_{\mathcal{C} \leftarrow \mathcal{B}}`$** is the $`m \times n`$ matrix:

$`[T]_{\mathcal{C} \leftarrow \mathcal{B}} = \begin{bmatrix} a_{11} & a_{12} & \dots & a_{1n} \\a_{21} & a_{22} & \dots & a_{2n} \\\vdots & \vdots & \ddots & \vdots \\a_{m1} & a_{m2} & \dots & a_{mn} \end{bmatrix}`$


Each **column** is the coordinate vector of $`T(\mathbf{v}_j)`$ relative to $`\mathcal{C}`$.

---

### **3. Finding the Matrix of a Linear Map Relative to Two Bases Given One Basis**

If the matrix of $`T`$ is known in standard bases (say, $`A`$) and we are given new bases $`\mathcal{B}`$ and $`\mathcal{C}`$, then:

$`[T]_{\mathcal{C} \leftarrow \mathcal{B}} = P_{\mathcal{C}}^{-1} A P_{\mathcal{B}}`$

Where:

* $`A`$ is the standard matrix of $`T`$


* $`P_{\mathcal{B}}`$ is the **change-of-basis matrix from $`\mathcal{B}`$ to the standard basis**


* $`P_{\mathcal{C}}`$ is the **change-of-basis matrix from $`\mathcal{C}`$ to the standard basis**


Alternatively:

* $`P_{\mathcal{B}}^{-1}`$: from standard basis to $`\mathcal{B}`$


* $`P_{\mathcal{C}}^{-1}`$: from standard basis to $`\mathcal{C}`$

---

### **4. Finding the Image of a Vector Under a Linear Map Given the Matrix Relative to Two Bases**

If:

* $`[T]_{\mathcal{C} \leftarrow \mathcal{B}}`$ is the matrix of $`T`$ relative to $`\mathcal{B}`$ and $`\mathcal{C}`$


* $`[\mathbf{v}]_{\mathcal{B}}`$ is the coordinate vector of $`\mathbf{v}`$ in basis $`\mathcal{B}`$



Then the **coordinate vector** of the image $`T(\mathbf{v})`$ in $`\mathcal{C}`$ is:


$`[T(\mathbf{v})]_{\mathcal{C}} = [T]_{\mathcal{C} \leftarrow \mathcal{B}} \cdot [\mathbf{v}]_{\mathcal{B}}`$


To get $`T(\mathbf{v})`$ in standard form, convert the result back using the basis $`\mathcal{C}`$:


$`T(\mathbf{v}) = P_{\mathcal{C}} \cdot [T(\mathbf{v})]_{\mathcal{C}}`$

---

### **5. Finding the Image of a Vector Given With Respect to the Standard Basis Under a Linear Map**

If:

* $`\mathbf{v} \in V`$ is expressed in standard coordinates


* $`A = [T]_{\text{std} \leftarrow \text{std}}`$ is the standard matrix of $`T`$

Then:

$`T(\mathbf{v}) = A \cdot \mathbf{v}`$

If the matrix of $T$ is given relative to other bases $`\mathcal{B}, \mathcal{C}`$, convert $`\mathbf{v}`$ to coordinates in $`\mathcal{B}`$, 
apply the matrix, then convert back from $`\mathcal{C}`$:


$`[\mathbf{v}]_{\mathcal{B}} = P_{\mathcal{B}}^{-1} \cdot \mathbf{v}`$


$`[T(\mathbf{v})]_{\mathcal{C}} = [T]_{\mathcal{C} \leftarrow \mathcal{B}} \cdot [\mathbf{v}]_{\mathcal{B}}`$


$`T(\mathbf{v}) = P_{\mathcal{C}} \cdot [T(\mathbf{v})]_{\mathcal{C}}`$

---

### **Summary Table**

| **Task**                            | **Formula / Method**                                                                                          |
| ----------------------------------- |---------------------------------------------------------------------------------------------------------------|
| Matrix from definition              | Columns are $`[T(\mathbf{v}_j)]_{\mathcal{C}}`$                                                               |
| Matrix from standard                | $`[T]_{\mathcal{C} \leftarrow \mathcal{B}} = P_{\mathcal{C}}^{-1} A P_{\mathcal{B}}`$                         |
| Image from matrix & vector in bases | $`[T(\mathbf{v})]_{\mathcal{C}} = [T]_{\mathcal{C} \leftarrow \mathcal{B}} \cdot [\mathbf{v}]_{\mathcal{B}}`$ |
| Image from standard matrix          | $`T(\mathbf{v}) = A \cdot \mathbf{v}`$                                                                        |
| Change-of-basis (std to basis)      | $`[\mathbf{v}]_{\mathcal{B}} = P_{\mathcal{B}}^{-1} \cdot \mathbf{v}`$                                        |
| Change-of-basis (basis to std)      | $`\mathbf{v} = P_{\mathcal{B}} \cdot [\mathbf{v}]_{\mathcal{B}}`$                                             |

---

