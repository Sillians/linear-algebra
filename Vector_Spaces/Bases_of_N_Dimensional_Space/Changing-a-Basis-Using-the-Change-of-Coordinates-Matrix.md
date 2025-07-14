## **Changing a Basis Using the Change-of-Coordinates Matrix**

---

### **1. Overview: Changing Bases**

A **change of basis** allows us to represent a vector in terms of a new coordinate system. 
This is essential in simplifying linear transformations, solving differential equations, and understanding geometric structures.

If a vector is originally represented in basis $`\mathcal{B}`$, and we want to express it in basis $`\mathcal{C}`$, we use a **change-of-coordinates matrix**.

---

### **2. Change-of-Coordinates Matrix Definition**

Let $`P_{\mathcal{C} \leftarrow \mathcal{B}}`$ be the **change-of-coordinates matrix** from basis $`\mathcal{B}`$ to 
basis $`\mathcal{C}`$. It transforms coordinates in $`\mathcal{B}`$ to coordinates in $`\mathcal{C}`$:


$`[\mathbf{x}]_{\mathcal{C}} = P_{\mathcal{C} \leftarrow \mathcal{B}} \cdot [\mathbf{x}]_{\mathcal{B}}`$


If $`P_{\mathcal{B} \leftarrow \mathcal{C}}`$ is the inverse of this matrix, then:


$`[\mathbf{x}]_{\mathcal{B}} = P_{\mathcal{B} \leftarrow \mathcal{C}} \cdot [\mathbf{x}]_{\mathcal{C}} = \left(P_{\mathcal{C} \leftarrow \mathcal{B}}\right)^{-1} \cdot [\mathbf{x}]_{\mathcal{C}}`$

---

### **3. Finding the Coordinates of a Vector in a New Basis Given the Change-of-Coordinates Matrix**

Given:

* $`[\mathbf{x}]_{\mathcal{B}}`$


* $`P_{\mathcal{C} \leftarrow \mathcal{B}}`$


Then:

$`[\mathbf{x}]_{\mathcal{C}} = P_{\mathcal{C} \leftarrow \mathcal{B}} \cdot [\mathbf{x}]_{\mathcal{B}}`$

#### **Example**:

Let

$`[\mathbf{x}]_{\mathcal{B}} = \begin{bmatrix}2\\-1\end{bmatrix}, \quad P_{\mathcal{C} \leftarrow \mathcal{B}} = \begin{bmatrix}1 & 3\\0 & 2\end{bmatrix}`$

Then:

$`[\mathbf{x}]_{\mathcal{C}} = \begin{bmatrix}1 & 3\\0 & 2\end{bmatrix} \begin{bmatrix}2\\-1\end{bmatrix} = \begin{bmatrix}-1\\-2\end{bmatrix}`$

---

### **4. Finding the Coordinates of a Vector in a New Basis Given the Inverse Change-of-Coordinates Matrix**

Given:

* $`[\mathbf{x}]_{\mathcal{C}}`$


* $`P_{\mathcal{B} \leftarrow \mathcal{C}} = \left(P_{\mathcal{C} \leftarrow \mathcal{B}}\right)^{-1}`$

Then:

$`[\mathbf{x}]_{\mathcal{B}} = P_{\mathcal{B} \leftarrow \mathcal{C}} \cdot [\mathbf{x}]_{\mathcal{C}}`$

Or:

$`[\mathbf{x}]_{\mathcal{B}} = \left(P_{\mathcal{C} \leftarrow \mathcal{B}}\right)^{-1} \cdot [\mathbf{x}]_{\mathcal{C}}`$

---

### **5. Finding the Coordinates of a Vector in a New Basis Given Its Coordinates in the Standard Basis**

Let $`\mathcal{B} = \{\mathbf{b}_1, \dots, \mathbf{b}_n\}`$ be a basis. Construct the matrix:


$`P_{\mathcal{B}} = \begin{bmatrix} \mathbf{b}_1 & \dots & \mathbf{b}_n \end{bmatrix}`$


Then for $`\mathbf{x} \in \mathbb{R}^n`$, its coordinates in $`\mathcal{B}`$ are:


$`[\mathbf{x}]_{\mathcal{B}} = P_{\mathcal{B}}^{-1} \cdot \mathbf{x}`$

---

### **6. Finding the Coordinates of a Vector in a New Basis Given Its Coordinates in Another Basis**

Given:

* $`[\mathbf{x}]_{\mathcal{B}}`$


* Change-of-coordinates matrix $`P_{\mathcal{C} \leftarrow \mathcal{B}}`$


Then:

$`[\mathbf{x}]_{\mathcal{C}} = P_{\mathcal{C} \leftarrow \mathcal{B}} \cdot [\mathbf{x}]_{\mathcal{B}}`$


To move **back**:

$`[\mathbf{x}]_{\mathcal{B}} = P_{\mathcal{B} \leftarrow \mathcal{C}} \cdot [\mathbf{x}]_{\mathcal{C}} = \left(P_{\mathcal{C} \leftarrow \mathcal{B}}\right)^{-1} \cdot [\mathbf{x}]_{\mathcal{C}}`$

---

### **Summary Table**

| **Task**                             | **Formula**                                                                                                              |
| ------------------------------------ | ------------------------------------------------------------------------------------------------------------------------ |
| From $`\mathcal{B}`$ to $`\mathcal{C}`$  | $`[\mathbf{x}]_{\mathcal{C}} = P_{\mathcal{C} \leftarrow \mathcal{B}} \cdot [\mathbf{x}]_{\mathcal{B}}`$                   |
| From $`\mathcal{C}`$ to $`\mathcal{B}`$  | $`[\mathbf{x}]_{\mathcal{B}} = \left(P_{\mathcal{C} \leftarrow \mathcal{B}}\right)^{-1} \cdot [\mathbf{x}]_{\mathcal{C}}`$ |
| From standard basis to $`\mathcal{B}`$ | $`[\mathbf{x}]_{\mathcal{B}} = P_{\mathcal{B}}^{-1} \cdot \mathbf{x}`$                                                     |
| From $`\mathcal{B}`$ to standard basis | $`\mathbf{x} = P_{\mathcal{B}} \cdot [\mathbf{x}]_{\mathcal{B}}`$                                                          |

