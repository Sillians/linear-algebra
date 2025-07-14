## **The Change-of-Coordinates Matrix**

---

### **Overview**

A **Change-of-Coordinates Matrix** (also called a transition matrix) is used in linear algebra to convert vector 
representations from one basis to another. If a vector has coordinates in one basis, and we want its coordinates
in another basis, we apply the appropriate change-of-coordinates matrix.

---

### **1. Basic Definitions**

Let:

* $`\mathcal{B} = \{ \mathbf{b}_1, \dots, \mathbf{b}_n \}`$ be a basis of a vector space $V$


* $`\mathcal{C} = \{ \mathbf{c}_1, \dots, \mathbf{c}_n \}`$ be another basis of $V$

Then, the **change-of-coordinates matrix** from $\mathcal{B}$ to $`\mathcal{C}`$ is denoted by:

$`P_{\mathcal{C} \leftarrow \mathcal{B}}`$

This matrix satisfies:

$`[\mathbf{v}]_{\mathcal{C}} = P_{\mathcal{C} \leftarrow \mathcal{B}} \cdot [\mathbf{v}]_{\mathcal{B}}`$

---

### **2. Finding the Change-of-Coordinates Matrix Given a Linear Connection Between Two Bases**

Suppose you know each $`\mathbf{b}_i`$ in terms of $`\mathcal{C}`$:


$`\mathbf{b}_1 = a_{11} \mathbf{c}_1 + \dots + a_{1n} \mathbf{c}_n \\\mathbf{b}_2 = a_{21} \mathbf{c}_1 + \dots + a_{2n} \mathbf{c}_n \\\vdots \\\mathbf{b}_n = a_{n1} \mathbf{c}_1 + \dots + a_{nn} \mathbf{c}_n`$


Then the change-of-coordinates matrix $`P_{\mathcal{C} \leftarrow \mathcal{B}}`$ is the matrix whose columns are the 
coordinates of the $`\mathbf{b}_i`$ vectors **expressed in the $`\mathcal{C}`$-basis**.

$`P_{\mathcal{C} \leftarrow \mathcal{B}} = \begin{bmatrix}[\mathbf{b}_1]_{\mathcal{C}} & \cdots & [\mathbf{b}_n]_{\mathcal{C}} \end{bmatrix}`$

---

### **3. Finding the Change-of-Coordinates Matrix When One of the Bases is the Standard Basis**

Let $`\mathcal{E} = \{ \mathbf{e}_1, \dots, \mathbf{e}_n \}`$ be the standard basis for $`\mathbb{R}^n`$, 
and let $`\mathcal{B} = \{ \mathbf{b}_1, \dots, \mathbf{b}_n \}`$ be another basis.

* Then:

$`P_{\mathcal{E} \leftarrow \mathcal{B}} = \begin{bmatrix} \mathbf{b}_1 & \mathbf{b}_2 & \cdots & \mathbf{b}_n \end{bmatrix}`$


This matrix maps $`\mathcal{B}`$-coordinates to standard coordinates:


$`[\mathbf{v}]_{\mathcal{E}} = P_{\mathcal{E} \leftarrow \mathcal{B}} \cdot [\mathbf{v}]_{\mathcal{B}}`$


To go **from standard coordinates to $`\mathcal{B}`$-coordinates**, invert the matrix:


$`P_{\mathcal{B} \leftarrow \mathcal{E}} = P_{\mathcal{E} \leftarrow \mathcal{B}}^{-1}`$

---

### **4. Using the Invertibility Property of the Change-of-Coordinates Matrix**

If $`\mathcal{B}`$ and $`\mathcal{C}`$ are both bases (i.e., sets of linearly independent vectors), 
then the change-of-coordinates matrix is **invertible**:

$`P_{\mathcal{B} \leftarrow \mathcal{C}} = \left( P_{\mathcal{C} \leftarrow \mathcal{B}} \right)^{-1}`$

This means that you can reverse the transformation between coordinate systems by using the matrix inverse.

---

### **5. Finding the Change-of-Coordinates Matrix Between Two Bases**

Let $`\mathcal{B} = \{ \mathbf{b}_1, \dots, \mathbf{b}_n \}`$ and $`\mathcal{C} = \{ \mathbf{c}_1, \dots, \mathbf{c}_n \}`$ be two bases of $`\mathbb{R}^n`$.

**Steps:**

1. Form the matrix:

$$
B = \begin{bmatrix}
\mathbf{b}_1 & \cdots & \mathbf{b}_n
\end{bmatrix}
\quad \text{and} \quad
C = \begin{bmatrix}
\mathbf{c}_1 & \cdots & \mathbf{c}_n
\end{bmatrix}
$$

2. Compute the matrix that changes coordinates from $`\mathcal{B}`$ to $`\mathcal{C}`$:

$$
P_{\mathcal{C} \leftarrow \mathcal{B}} = C^{-1} B
$$

This gives the transformation that maps a vector's $`\mathcal{B}`$-coordinates to its $`\mathcal{C}`$-coordinates.

---

### **Summary Table**

| **From Basis**           | **To Basis**             | **Matrix**                                          | **Operation**                                  |
| ------------------------ | ------------------------ | --------------------------------------------------- | ---------------------------------------------- |
| $`\mathcal{B}`$            | $`\mathcal{C}`$            | $`P_{\mathcal{C} \leftarrow \mathcal{B}} = C^{-1} B`$ | $`[v]_{\mathcal{C}} = P [v]_{\mathcal{B}}`$      |
| $`\mathcal{C}`$            | $`\mathcal{B}`$            | $`P_{\mathcal{B} \leftarrow \mathcal{C}} = B^{-1} C`$ | $`[v]_{\mathcal{B}} = P [v]_{\mathcal{C}}`$      |
| $`\mathcal{B}`$            | standard ($`\mathcal{E}`$) | $`P_{\mathcal{E} \leftarrow \mathcal{B}} = B`$        | $`[v]_{\mathcal{E}} = B [v]_{\mathcal{B}}`$      |
| standard ($`\mathcal{E}`$) | $`\mathcal{B}`$            | $`P_{\mathcal{B} \leftarrow \mathcal{E}} = B^{-1}`$   | $`[v]_{\mathcal{B}} = B^{-1} [v]_{\mathcal{E}}`$ |


