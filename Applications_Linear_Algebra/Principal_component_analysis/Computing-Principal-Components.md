## **Computing Principal Components**

---

### **1. What Are Principal Components?**

Principal components are **orthogonal directions** in the data along which the variance is **maximized**. 
They are derived from the **eigenvectors of the covariance matrix** of a dataset, ordered by descending eigenvalues.


* The **first principal component (PC1)** is the direction of **maximum variance**.


* The **second principal component (PC2)** is orthogonal to the first and captures the next most variance.


* And so on...

---

### **2. Principal Components and the Covariance Matrix**

Given a **zero-mean** data matrix $`X \in \mathbb{R}^{n \times d}`$, the **covariance matrix** is:

$$
\Sigma = \frac{1}{n} X^\top X
$$

To find the principal components, **solve the eigenvalue problem**:

$$
\Sigma v = \lambda v
$$

* Eigenvectors $v$: directions (principal components)
* Eigenvalues $`\lambda`$: variances explained along those directions

---

### **3. Finding a Principal Component Given a 2x2 Covariance Matrix**

#### **Example:**

Let

$$
\Sigma = 
\begin{bmatrix}
4 & 2 \\
2 & 3
\end{bmatrix}
$$

#### **Step 1: Characteristic Equation**

$$
\det(\Sigma - \lambda I) = 0
\Rightarrow 
\begin{vmatrix}
4 - \lambda & 2 \\
2 & 3 - \lambda
\end{vmatrix}
= (4 - \lambda)(3 - \lambda) - 4 = 0
$$

$$
\lambda^2 - 7\lambda + 8 = 0 \Rightarrow \lambda = 4.561, 2.439
$$

#### **Step 2: Eigenvectors**

For $`\lambda = 4.561`$, solve:

$$
(\Sigma - \lambda I)v = 0 \Rightarrow
\begin{bmatrix}
-0.561 & 2 \\
2 & -1.561
\end{bmatrix}
\begin{bmatrix}
v_1 \\
v_2
\end{bmatrix}
= 0
\Rightarrow v = \begin{bmatrix} 0.850 \\ 0.526 \end{bmatrix}
$$

So:

* **First principal component**: direction $[0.850, 0.526]^\top$
* **Variance explained**: 4.561

---

### **4. Finding a Principal Component Given a 3x3 Covariance Matrix**

#### **Example:**

$$
\Sigma =
\begin{bmatrix}
2 & 0 & 1 \\
0 & 3 & 0 \\
1 & 0 & 2
\end{bmatrix}
$$

#### **Step 1: Solve $\det(\Sigma - \lambda I) = 0$**

$$
\det
\begin{bmatrix}
2 - \lambda & 0 & 1 \\
0 & 3 - \lambda & 0 \\
1 & 0 & 2 - \lambda
\end{bmatrix}
= (3 - \lambda)[(2 - \lambda)^2 - 1]
\Rightarrow \lambda = 1, 2, 3
$$

#### **Step 2: Eigenvectors**

* For $`\lambda = 3`$: $`v = [0, 1, 0]`$ — PC1 (along $y$-axis)


* For $`\lambda = 2`$: $`v = [1, 0, -1]`$ (normalize it)


* For $`\lambda = 1`$: $`v = [1, 0, 1]`$ (normalize it)

---

### **5. Summary Table**

| Step | Description                                               |
| ---- | --------------------------------------------------------- |
| 1    | Form the covariance matrix $`\Sigma`$ from centered data    |
| 2    | Solve $`\Sigma v = \lambda v`$ for eigenvalues/eigenvectors |
| 3    | Sort eigenvectors by decreasing eigenvalues               |
| 4    | Principal components = ordered eigenvectors               |
| 5    | Variance explained by each = corresponding eigenvalue     |

---

### **6. Applications**

| Area                         | Use                                    |
| ---------------------------- | -------------------------------------- |
| **Dimensionality Reduction** | Keep top $k$ PCs to reduce noise       |
| **Visualization**            | Project high-dimensional data to 2D/3D |
| **Compression**              | Efficient data encoding                |
| **Feature Engineering**      | Use PCs as uncorrelated features       |

---
