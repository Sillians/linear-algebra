## **Expressing the Coordinates of a Vector in a Given Basis**

This guide explores how vectors can be expressed in terms of a different basis, including techniques for finding coordinates and reconstructing vectors from coordinates.

---

### **1. What Does "Coordinates in a Basis" Mean?**

Given a vector space and a basis $`\mathcal{B} = {\mathbf{v}\_1, \mathbf{v}\_2, \dots, \mathbf{v}\_n}`$, 
every vector $`\mathbf{x}`$ in that space can be **uniquely written** as a linear combination:

$`\mathbf{x} = c_1\mathbf{v}_1 + c_2\mathbf{v}_2 + \dots + c_n\mathbf{v}_n`$

The **coordinates of $`\mathbf{x}`$ relative to the basis $`\mathcal{B}`$** are the scalars $`(c\_1, c\_2, \dots, c\_n)`$.

---

### **2. Finding a Vector Given Its Coordinates Relative to a Basis**

Given coordinates $`(c\_1, c\_2, \dots, c\_n)`$ and basis vectors $`{\mathbf{v}\_1, \mathbf{v}\_2, \dots, \mathbf{v}\_n}`$:

$`\mathbf{x} = c_1\mathbf{v}_1 + c_2\mathbf{v}_2 + \dots + c_n\mathbf{v}_n`$

**Example:**

Let $`\mathcal{B} = \left\{ \begin{pmatrix} 1 \\ 0 \end{pmatrix}, \begin{pmatrix} 1 \\ 1 \end{pmatrix} \right\}`$ and coordinates $`[2, -1]\_{\mathcal{B}}`$.


Then:

$`\mathbf{x} = 2\begin{bmatrix}1\\0\end{bmatrix} + (-1)\begin{bmatrix}1\\1\end{bmatrix} = \begin{bmatrix}2\\0\end{bmatrix} + \begin{bmatrix}-1\\-1\end{bmatrix} = \begin{bmatrix}1\\-1\end{bmatrix}`$

---

### **3. Finding the Coordinates of a Vector Relative to a Given Basis by Inspection**

If $`\mathbf{x}`$ is clearly a linear combination of basis vectors, inspect and solve.

**Example:**

$`\mathcal{B} = \left\{ \begin{pmatrix} 1 \\ 0 \end{pmatrix}, \begin{pmatrix} 0 \\ 1 \end{pmatrix} \right\}`$  

and the vector: $`\mathbf{x} = \begin{pmatrix} 4 \\ 3 \end{pmatrix}`$


Since $`\mathbf{x} = 4\mathbf{v}\_1 + 3\mathbf{v}\_2`$, the coordinates are:


$`[ \mathbf{x} ]_{\mathcal{B}} = \begin{bmatrix}4\\3\end{bmatrix}`$

---

### **4. Finding the Coordinates of a Vector Relative to a Basis Containing Two Vectors**

Given $`\mathcal{B} = {\mathbf{v}\_1, \mathbf{v}\_2}`$ and a vector $`\mathbf{x}`$, solve:

$`\mathbf{x} = c_1\mathbf{v}_1 + c_2\mathbf{v}_2`$

Set up and solve the system:

$`\mathbf{x} = [\mathbf{v}_1 \ \mathbf{v}_2] \begin{bmatrix} c_1 \\ c_2 \end{bmatrix}`$

**Example:**

Let $`\mathbf{x} = \begin{pmatrix} 3 \\ 5 \end{pmatrix}`$  

and $`\mathcal{B} = \left\{ \begin{pmatrix} 1 \\ 2 \end{pmatrix}, \begin{pmatrix} 1 \\ 1 \end{pmatrix} \right\}`$


Solve:

$`\begin{bmatrix}3\\5\end{bmatrix} = c_1\begin{bmatrix}1\\2\end{bmatrix} + c_2\begin{bmatrix}1\\1\end{bmatrix} = \begin{bmatrix}c_1 + c_2\\ 2c_1 + c_2\end{bmatrix}`$

Equating:

* $`c\_1 + c\_2 = 3`$
* $`2c\_1 + c\_2 = 5`$

Solving gives $`c\_1 = 2`$, $`c\_2 = 1`$, so:

$`[\mathbf{x}]_{\mathcal{B}} = \begin{bmatrix}2\\1\end{bmatrix}`$

---

### **5. Finding the Coordinates of a Vector Relative to a Basis Containing More Than Two Vectors**

Same approach as above, extended to more variables:

Given $`\mathcal{B} = {\mathbf{v}\_1, \mathbf{v}\_2, \mathbf{v}\_3}`$ and $`\mathbf{x}`$, solve:


$`\mathbf{x} = c_1\mathbf{v}_1 + c_2\mathbf{v}_2 + c_3\mathbf{v}_3`$



**Example:**

Let $`\mathbf{x} = \begin{pmatrix} 1 \\ 4 \\ 3 \end{pmatrix}`$  

and

$$\mathcal{B} = \lbrace\{ 
\begin{pmatrix} 1 \\ 0 \\ 0 \end{pmatrix},\ 
\begin{pmatrix} 0 \\ 1 \\ 1 \end{pmatrix},\ 
\begin{pmatrix} 0 \\ 1 \\ -1 \end{pmatrix} 
\rbrace\}$$


Write:

$`\begin{bmatrix}1\\4\\3\end{bmatrix} = c_1\begin{bmatrix}1\\0\\0\end{bmatrix} + c_2\begin{bmatrix}0\\1\\1\end{bmatrix} + c_3\begin{bmatrix}0\\1\\-1\end{bmatrix}`$

Combine:

$`= \begin{bmatrix}c_1\\ c_2 + c_3\\ c_2 - c_3\end{bmatrix}`$

Equating:

* $`c\_1 = 1`$
* $`c\_2 + c\_3 = 4`$
* $`c\_2 - c\_3 = 3`$

Solving:

* Add: $`2c\_2 = 7 \Rightarrow c\_2 = \frac{7}{2}`$
* Then $`c\_3 = \frac{1}{2}`$

So:

$`[\mathbf{x}]_{\mathcal{B}} = \begin{bmatrix}1\\ \frac{7}{2}\\ \frac{1}{2}\end{bmatrix}`$

---

### **6. Summary Table**

| Task                                                             | Method                                           |
| ---------------------------------------------------------------- |--------------------------------------------------|
| Given coordinates in basis → find vector                         | Linear combination of basis vectors              |
| Given vector → coordinates in standard basis                     | Direct components (if standard basis)            |
| Given vector → coordinates in custom basis (2 vectors)           | Solve $`Ax = b`$ with 2 columns                  |
| Given vector → coordinates in custom basis (more than 2 vectors) | Solve $`Ax = b`$ with more columns               |
| Basis vectors are linearly independent                           | Coordinates are unique                           |
| Basis vectors form invertible matrix                             | Use $`\left[ x \right]_{\mathcal{B}} = A^{-1}x`$ |

---

### **Conclusion**

Changing the basis is fundamental to understanding linear algebra. It underpins concepts like diagonalization, 
eigenvectors, and transformations across different coordinate systems. Mastery of computing and interpreting 
vector coordinates relative to a basis allows deep insight into the structure of vector spaces.

