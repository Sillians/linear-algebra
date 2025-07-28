## **The Matrix of a Linear Transformation Relative to a Basis**

---

### **1. Core Idea**

Given a linear transformation $`T: V \to V`$ (or $`T: V \to W`$) and a basis $`\mathcal{B} = {v\_1, \dots, v\_n}`$ for $`V`$, 
we define the **matrix of $`T`$ relative to the basis $`\mathcal{B}`$** as the matrix that captures the action of $`T`$ on 
arbitrary vectors in terms of their coordinates in $`\mathcal{B}`$.

---

### **2. Formal Definition**

Let $`\mathcal{B} = {v\_1, \dots, v\_n}`$ be a basis of $V$. The matrix of $`T\$ relative to \$\mathcal{B}`$, denoted $`[T]\_{\mathcal{B}}`$, 
is the matrix whose $`j\`$-th column is the coordinate vector of $`T(v\_j)`$ with respect to $`\mathcal{B}`$:


$`[T]_{\mathcal{B}} = \begin{bmatrix} [T(v_1)]_{\mathcal{B}} & [T(v_2)]_{\mathcal{B}} & \cdots & [T(v_n)]_{\mathcal{B}} \end{bmatrix}`$

---

### **3. Key Computations**

#### **a. Calculating the Image of a Vector Given the Matrix of a Linear Transformation Relative to a Basis**

Let $`[T]*{\mathcal{B}}`$ be the matrix of $`T`$ relative to basis $`\mathcal{B}`$, and suppose $`[x]*{\mathcal{B}}`$ is the coordinate vector 
of $`x \in V`$ relative to $`\mathcal{B}`$. Then:


$`[T(x)]_{\mathcal{B}} = [T]_{\mathcal{B}} \cdot [x]_{\mathcal{B}}`$


To recover $`T(x)`$ in standard coordinates, apply the inverse change-of-basis transformation if needed.

---

#### **b. Finding the Matrix of a Linear Transformation Given the Images of the Basis Vectors**

Let $`\mathcal{B} = {v\_1, v\_2, \dots, v\_n}`$ and suppose $`T(v\_j)`$ is known for each $`j`$.

1. Express $`T(v\_j)`$ in terms of the basis $`\mathcal{B}`$:

   $`T(v_j) = a_{1j}v_1 + a_{2j}v_2 + \cdots + a_{nj}v_n`$


2. Then the $j$-th column of $`[T]\_{\mathcal{B}}`$ is:

   $`[T(v_j)]_{\mathcal{B}} = \begin{bmatrix} a_{1j} \\ a_{2j} \\ \vdots \\ a_{nj} \end{bmatrix}`$

---

#### **c. Finding the Matrix of a Linear Transformation Relative to a Basis in a Two-Dimensional Vector Space**

Suppose $`\mathcal{B} = {v\_1, v\_2}`$ and $`T: V \to V`$ with $`T(v\_1) = a\_{11}v\_1 + a\_{21}v\_2`$, $`T(v\_2) = a\_{12}v\_1 + a\_{22}v\_2`$. Then:


$`[T]_{\mathcal{B}} = \begin{bmatrix} a_{11} & a_{12} \\a_{21} & a_{22} \end{bmatrix}`$


---

#### **d. Finding the Matrix of a Linear Transformation Relative to a Basis in a Three-Dimensional Vector Space**

Let $`\mathcal{B} = {v\_1, v\_2, v\_3}`$ and suppose:

* $`T(v\_1) = a\_{11}v\_1 + a\_{21}v\_2 + a\_{31}v\_3`$


* $`T(v\_2) = a\_{12}v\_1 + a\_{22}v\_2 + a\_{32}v\_3`$


* $`T(v\_3) = a\_{13}v\_1 + a\_{23}v\_2 + a\_{33}v\_3`$

Then:


$`[T]_{\mathcal{B}} = \begin{bmatrix} a_{11} & a_{12} & a_{13} \\a_{21} & a_{22} & a_{23} \\a_{31} & a_{32} & a_{33} \end{bmatrix}`$


---

### **4. Coordinate Conversion**

* To convert a vector $`v`$ from standard coordinates to coordinates relative to basis $`\mathcal{B}`$: Solve $`P\_{\mathcal{B}} [v]*{\mathcal{B}} = v`$ for $`[v]*{\mathcal{B}}`$, where $`P\_{\mathcal{B}}`$ is the **change-of-basis matrix**.

* To go from $`[T(v)]\_{\mathcal{B}}`$ to $`T(v)`$ in standard coordinates:

  $`T(v) = P_{\mathcal{B}} [T(v)]_{\mathcal{B}}`$

---

### **5. Summary Table**

| Task                                       | Method                                                             |
|--------------------------------------------|--------------------------------------------------------------------|
| Matrix of $`T`$ relative to $`mathcal{B}`$ | Columns are $`[T(v\_j)]\_{\mathcal{B}}`$                           |
| Image of $`x`$ under $`T`$ in coordinates  | $`[T(x)]*{\mathcal{B}} = [T]*{\mathcal{B}} \cdot [x]\_{\mathcal{B}}`$ |
| Convert to standard coordinates            | Multiply by basis matrix $`P\_{\mathcal{B}}`$                       |
| 2D Matrix Example                          | $`[T]\_{\mathcal{B}}`$ is $`2 \times 2`$                           |
| 3D Matrix Example                          | $`[T]\_{\mathcal{B}}`$ is $`3 \times 3`$                           |

---
