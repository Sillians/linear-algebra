## **The Connection Between PCA and SVD**

---

### **1. Overview**

**Principal Component Analysis (PCA)** and **Singular Value Decomposition (SVD)** are two foundational techniques in linear algebra and data analysis, 
closely connected through matrix factorization and dimensionality reduction.


* **PCA** identifies orthogonal directions (principal components) that capture maximum variance in the data.


* **SVD** factorizes a matrix into orthogonal directions of input and output (row/column spaces), enabling efficient computation of PCA.

---

### **2. PCA and the Covariance Matrix**

Given a **centered** data matrix $`X \in \mathbb{R}^{n \times d}`$ (each row is an observation, each column a feature):


$$
\text{Covariance matrix: } C = \frac{1}{n} X^\top X
$$


PCA involves:

* **Eigenvalue decomposition** of $C$


* Eigenvectors → principal components


* Eigenvalues → variances explained

---


### **3. SVD of the Observation Matrix**

SVD decomposes the matrix $`X \in \mathbb{R}^{n \times d}`$ as:

$$
X = U \Sigma V^\top
$$


Where:

* $`U \in \mathbb{R}^{n \times n}`$: left singular vectors (orthonormal)


* $`\Sigma \in \mathbb{R}^{n \times d}`$: diagonal matrix of singular values $`\sigma_1 \ge \sigma_2 \ge \cdots`$


* $`V \in \mathbb{R}^{d \times d}`$: right singular vectors (orthonormal)

---

### **4. Connecting PCA and SVD**

$$
X^\top X = V \Sigma^\top \Sigma V^\top \quad \Rightarrow \quad \text{Covariance matrix shares eigenvectors with } V
$$


So:

* **Principal components** = **right singular vectors** (columns of $V$)


* **Explained variance** by each component = $`\frac{\sigma_i^2}{n}`$

---

### **5. Finding a Principal Component Given the SVD of the Observation Matrix**

If:

$$
X = U \Sigma V^\top
$$


Then:

* **First principal component** = first column of $V$


* **Second principal component** = second column of $V$


* And so on...


Each principal component is a **direction** (a unit vector) in the original feature space.



#### **Example:**

Let:

$$
X = U \Sigma V^\top \quad \text{with} \quad
V = 
\begin{bmatrix}
0.8 & -0.6 \\
0.6 & 0.8
\end{bmatrix}
$$

Then:

* PC1 = $`[0.8,\ 0.6]^\top`$


* PC2 = $`[-0.6,\ 0.8]^\top`$

---


### **6. Finding the Variance Given the SVD of the Observation Matrix**

The **variance explained** by each principal component is:

$$
\text{Variance explained by PC}_i = \frac{\sigma_i^2}{n}
$$

Where:

* $`\sigma_i`$ is the $`i^\text{th}`$ singular value


* $n$ is the number of observations (rows of $X$)

Total variance:

$$
\text{Total variance} = \frac{1}{n} \sum_{i=1}^{r} \sigma_i^2
$$

#### **Example:**

Let:

* $`\Sigma = \text{diag}(10, 5, 1)`$


* $`n = 100`$

Then:

* PC1 variance: $`\frac{10^2}{100} = 1`$


* PC2 variance: $`\frac{25}{100} = 0.25`$


* PC3 variance: $`\frac{1}{100} = 0.01`$

---

### **7. Summary Table**

| Concept                      | Formula                                                                       |
| ---------------------------- | ----------------------------------------------------------------------------- |
| SVD of $X$                   | $`X = U \Sigma V^\top`$                                                         |
| PCA directions               | Columns of $V$                                                                |
| Variance explained by PC$_i$ | $`\frac{\sigma_i^2}{n}`$                                                        |
| Covariance matrix            | $`\frac{1}{n} X^\top X = V \left( \frac{\Sigma^\top \Sigma}{n} \right) V^\top`$ |

---

### **8. Applications**

| Field                  | Use Case                                                        |
| ---------------------- | --------------------------------------------------------------- |
| Machine Learning       | Dimensionality reduction, visualization                         |
| Signal Processing      | Noise reduction, signal compression                             |
| Genomics               | Latent factor analysis                                          |
| Recommendation Systems | Latent embedding extraction (e.g., SVD in matrix factorization) |

---
