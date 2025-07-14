# **Introduction to Principal Component Analysis (PCA)**

---

## **1. What is PCA?**

**Principal Component Analysis (PCA)** is a **dimensionality reduction technique** used to:

* Simplify large datasets
* Extract relevant patterns
* Reduce noise or redundancy
* Visualize high-dimensional data in 2D or 3D

PCA transforms the original correlated features into a new set of **uncorrelated variables** called **principal components**, ordered by the amount of **variance** they explain.

---

## **2. Intuition Behind PCA**

PCA finds directions (axes) in the feature space that:

* **Maximize the variance** of projected data
* Are **orthogonal** to each other

These directions are the **eigenvectors** of the data's **covariance matrix**, and the variances along them are the **eigenvalues**.

---

## **3. Mathematical Steps of PCA**

### Step 1: Mean Centering the Data

Given a dataset $`X \in \mathbb{R}^{n \times d}`$, subtract the mean from each feature:

$$
\tilde{X} = X - \bar{X}
$$

---

### Step 2: Compute the Covariance Matrix

$$
\Sigma = \frac{1}{n - 1} \tilde{X}^T \tilde{X}
$$

---

### Step 3: Compute Eigenvalues and Eigenvectors

Solve:

$$
\Sigma \mathbf{v}_i = \lambda_i \mathbf{v}_i
$$

Where:

* $`\lambda_i`$: variance explained by the $`i`$-th principal component
* $`\mathbf{v}_i`$: direction of the $`i`$-th principal component

---

### Step 4: Select Top **k** Components

Order eigenvectors by descending eigenvalues and select the top $k$:

$$
V_k = [\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_k]
$$

---

### Step 5: Project Data to New Subspace

Transform the data:

$$
Z = \tilde{X} V_k
$$

Where:

* $`Z`$ is the reduced data in $`k`$ dimensions

---

## **4. Key Properties of PCA**

* The **first principal component** captures the **maximum variance**.
* Each succeeding component is **orthogonal** to the previous ones.
* PCA assumes **linear relationships**.
* PCA is sensitive to **scaling** of the input features.

---

## **5. Applications of PCA**

* Data **visualization**
* **Noise filtering**
* **Feature extraction** before modeling
* **Compression** of high-dimensional datasets
* **Preprocessing** for clustering or regression

---

## Summary

| Concept              | Description                                        |
| -------------------- | -------------------------------------------------- |
| PCA                  | Dimensionality reduction via variance maximization |
| Principal components | New uncorrelated axes (eigenvectors of covariance) |
| Variance explained   | Proportional to eigenvalues                        |
| Projection           | $`Z = \tilde{X} V_k`$                                |
| Key assumptions      | Linearity, large variances = important structures  |

---
