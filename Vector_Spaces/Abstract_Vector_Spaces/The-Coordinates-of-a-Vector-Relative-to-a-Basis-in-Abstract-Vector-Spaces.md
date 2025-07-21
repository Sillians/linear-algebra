## **The Coordinates of a Vector Relative to a Basis in Abstract Vector Spaces**

---

### **1. Understanding Coordinates Relative to a Basis**

In any abstract vector space $V$, a **basis** is a linearly independent set of vectors that spans the space. 
Given a basis $`\mathcal{B} = \{ \mathbf{v}_1, \mathbf{v}_2, \dots, \mathbf{v}_n \}`$, any vector $`\mathbf{x} \in V`$ can be uniquely expressed as:


$`\mathbf{x} = c_1 \mathbf{v}_1 + c_2 \mathbf{v}_2 + \cdots + c_n \mathbf{v}_n`$


The **coordinates of $`\mathbf{x}`$** relative to the basis $`\mathcal{B}`$ are:


$`[\mathbf{x}]_\mathcal{B} = \begin{bmatrix} c_1 \\ c_2 \\ \vdots \\ c_n \end{bmatrix}`$

---

### **2. Calculating a Vector Given Its Coordinates Relative to a Basis**

If a vector is given in terms of coordinates relative to a basis $`\mathcal{B}`$, the vector in standard form is found by performing a linear combination:


**Example**:

Let $`\mathcal{B} = \{ \mathbf{v}_1 = (1,0), \mathbf{v}_2 = (0,1) \}`$ and coordinates:


$`[\mathbf{x}]_\mathcal{B} = \begin{bmatrix} 2 \\ -3 \end{bmatrix}`$


Then the vector $`\mathbf{x}`$ is:


$`\mathbf{x} = 2\mathbf{v}_1 - 3\mathbf{v}_2 = 2(1,0) + (-3)(0,1) = (2,-3)`$

---

### **3. Finding Coordinates in a Matrix Vector Space**

Let $`\mathcal{B} = \{ A_1, A_2, \dots, A_k \}`$ be a basis of a subspace of $`M_{m \times n}`$, and $`A \in M_{m \times n}`$. 


The coordinates of $A$ with respect to $`\mathcal{B}`$ are scalars $`c_1, \dots, c_k`$ such that:


$`A = c_1 A_1 + c_2 A_2 + \cdots + c_k A_k`$


This is often solved by writing all matrices as vectors (flattened columnwise) and solving a linear system.


**Example**:


Let $`\mathcal{B} = \left\{ \begin{bmatrix}1 & 0 \\ 0 & 0\end{bmatrix}, \begin{bmatrix}0 & 1 \\ 0 & 0\end{bmatrix} \right\}`$


And $`A = \begin{bmatrix}3 & 5 \\ 0 & 0\end{bmatrix}`$


Then:

$`A = 3 \begin{bmatrix}1 & 0 \\ 0 & 0\end{bmatrix} + 5 \begin{bmatrix}0 & 1 \\ 0 & 0\end{bmatrix}`$


So $`[A]_\mathcal{B} = \begin{bmatrix}3 \\ 5 \end{bmatrix}`$

---

### **4. Finding Coordinates in a Polynomial Vector Space**

Let $`\mathcal{B} = \{1, x, x^2, \dots, x^{n-1}\}`$ be a basis for $`\mathbb{P}_{n-1}`$, and let:


$`p(x) = a_0 + a_1x + a_2x^2 + \cdots + a_{n-1}x^{n-1}`$


Then:


$`[p(x)]_\mathcal{B} = \begin{bmatrix} a_0 \\ a_1 \\ \vdots \\ a_{n-1} \end{bmatrix}`$


**Example**:

If $`p(x) = 2 + 4x - x^2`$ and $`\mathcal{B} = \{1, x, x^2\}`$, then:

$`[p(x)]_\mathcal{B} = \begin{bmatrix} 2 \\ 4 \\ -1 \end{bmatrix}`$

---

### **Summary Table**

| Context                         | Input                                          | Output                          |
| ------------------------------- |------------------------------------------------|---------------------------------|
| Coordinates from Basis Vectors  | $`c_1\mathbf{v}_1 + \cdots + c_n\mathbf{v}_n`$ | $`[\mathbf{x}]_\mathcal{B}`$    |
| Coordinates in Matrix Space     | Linear combination of basis matrices           | Vector of coefficients          |
| Coordinates in Polynomial Space | Polynomial written in powers of $x$            | Coefficients as a column vector |

---

This approach generalizes to any finite-dimensional vector space, including function spaces, matrix spaces, and polynomial spaces.
