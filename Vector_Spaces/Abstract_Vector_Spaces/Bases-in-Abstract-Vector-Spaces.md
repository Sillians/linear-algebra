## **Bases in Abstract Vector Spaces**

---

### **1. Overview of Bases in Abstract Vector Spaces**

In linear algebra, a **basis** of a vector space is a set of vectors that is both:

* **Linearly independent** (no vector is a linear combination of the others)


* **Spanning** (any vector in the space can be written as a linear combination of these vectors)


Every vector space has a basis, and all bases of a given vector space have the same number of elements—called the **dimension** of the vector space.


---

### **2. Identifying True Statements About Bases in Abstract Vector Spaces**

* A set is a **basis** if it spans the space and is linearly independent.


* A **basis** is not unique—there are infinitely many different bases.


* The **number of vectors in a basis** equals the **dimension** of the space.


* Any linearly independent set of vectors **equal in number to the dimension** of the space is a basis.


* Removing any vector from a basis makes it no longer a basis.

---

### **3. Polynomial Vector Spaces**

A **polynomial vector space** like $`\mathbb{P}_n`$ consists of all polynomials of degree at most $n$.

**Example**: The standard basis for $`\mathbb{P}_2`$ is:

$`\{1, x, x^2\}`$


#### **True Statements About Sets of Vectors in a Polynomial Vector Space**

* $`\{1, x, x^2\}`$ is a basis for $`\mathbb{P}_2`$.


* Any set of 3 linearly independent polynomials in $`\mathbb{P}_2`$ forms a basis.


* $`\{1, x, x^3\}`$ **is not** a basis for $`\mathbb{P}_2`$ because it doesn't span the space.

---


### **4. Matrix Vector Spaces**

A **matrix vector space** like $`M_{m \times n}`$ is the space of all $`m \times n`$ matrices with entries from a field (e.g., $`\mathbb{R}`$).

**Example**: $`M_{2 \times 2}`$ has dimension 4. 

A basis:

$`\left\{ \begin{bmatrix}1 & 0\\0 & 0\end{bmatrix}, \begin{bmatrix}0 & 1\\0 & 0\end{bmatrix}, \begin{bmatrix}0 & 0\\1 & 0\end{bmatrix}, \begin{bmatrix}0 & 0\\0 & 1\end{bmatrix} \right\}`$


#### **True Statements About Sets of Vectors in a Matrix Vector Space**

* Any 4 linearly independent $`2 \times 2`$ matrices form a basis for $`M_{2 \times 2}`$.


* Any set of fewer than 4 matrices **cannot** be a basis for $`M_{2 \times 2}`$.


* A set of 4 matrices is a basis **if and only if** they are linearly independent and span the space.

---

### **5. Summary Table**

| **Vector Space**                  | **Dimension**    | **Standard Basis**                                          |
|-----------------------------------|------------------|-------------------------------------------------------------|
| $`\mathbb{R}^n`$                  | $`n`$            | $`\{e_1, e_2, \dots, e_n\}`$                                |
| $`\mathbb{P}_n`$                  | $`n+1`$          | $`\{1, x, x^2, \dots, x^n\}`$                               |
| $`M_{m \times n}`$                | $`mn`$           | Matrices with a single 1 in each distinct position          |
| Function space (e.g., $`C[a,b]`$) | Infinite (often) | Depends on context (e.g., $`\{1, \sin x, \cos x, \dots\}`$) |

---

### **6. Final Note**

Understanding bases in abstract vector spaces generalizes the familiar idea from $`\mathbb{R}^n`$ to polynomials, matrices, and functions. 
The two key pillars—**linear independence** and **spanning**—remain essential across all these contexts.
