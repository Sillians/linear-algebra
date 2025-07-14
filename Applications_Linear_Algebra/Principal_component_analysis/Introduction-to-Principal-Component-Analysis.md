# **Principal Component Analysis (PCA)**

---

## **1. What Is PCA?**

**Principal Component Analysis (PCA)** is a **linear transformation** technique used in statistics and machine learning for:

* **Dimensionality reduction**
* **Pattern recognition**
* **Feature extraction**
* **Noise elimination**

It re-expresses the data in terms of **principal components** — new variables formed as **orthogonal linear combinations** of the original features that capture **maximum variance**.

---

## **2. Mathematical Foundation**

Given a dataset $`X \in \mathbb{R}^{n \times d}`$:

### **Step 1: Center the Data**

Remove the mean of each feature:

$$
\tilde{X} = X - \bar{X}
$$

---

### **Step 2: Compute the Covariance Matrix**

$$
\Sigma = \frac{1}{n - 1} \tilde{X}^T \tilde{X}
$$

---

### **Step 3: Perform Eigen Decomposition**

Find eigenvalues and eigenvectors:

$$
\Sigma \mathbf{v}_i = \lambda_i \mathbf{v}_i
$$

Where:

* $`\lambda_i`$ is the variance explained by the $`i`$-th principal component
* $`\mathbf{v}_i`$ is the direction of the $`i`$-th principal component

---

### **Step 4: Select Top **k** Principal Components**

Choose the top $`k`$ eigenvectors:

$$
V_k = [\mathbf{v}_1, \mathbf{v}_2, \dots, \mathbf{v}_k]
$$

---

### **Step 5: Project the Data**

Reduce dimensions:

$$
Z = \tilde{X} V_k
$$

---

## **3. Geometric Interpretation**

PCA finds a new basis in the feature space where:

* The **first principal component (PC1)** lies in the direction of **maximum variance**.
* The **second principal component (PC2)** is **orthogonal** to PC1 and captures the next highest variance.

---

## **4. Identifying the First Principal Component From a Scatter Plot**

### **How to Identify:**

* Look for the **direction** in which the data is **most spread out**.
* PC1 aligns along the **longest axis** of the data cloud.

### **Example:**

If data is stretched diagonally (say from bottom-left to top-right), then:

$$
\text{PC1} \propto \begin{bmatrix} 1 \\ 1 \end{bmatrix}
$$

---

## **5. Identifying the Second Principal Component From a Scatter Plot**

### **How to Identify:**

* PC2 lies **orthogonal** (perpendicular) to PC1.
* It captures the **next largest spread** in the data.

### **Example:**

If PC1 is along $`[1, 1]^T`$, then PC2 is likely along:

$$
\text{PC2} \propto \begin{bmatrix} 1 \\ -1 \end{bmatrix}
$$

(assuming normalized and orthogonal directions).

---

## **6. Interpreting Principal Components in Context**

### **Linear Combinations:**

Each principal component is a **weighted combination** of original features:

$$
\text{PC}_1 = w_{11}x_1 + w_{12}x_2 + \dots + w_{1d}x_d
$$

Where $`w_{1j}`$ are the components of the first eigenvector.

### **Interpretation Examples:**

* **Gene expression data**: PC1 may represent overall activity; PC2 may separate types of genes.
* **Marketing data**: PC1 could represent total spending; PC2 might capture the balance between categories.

Always **analyze the weights** (loadings) of the components to infer **what each principal component means** in terms of the original variables.

---

## Summary Table

| Concept               | Description                                                |
| --------------------- | ---------------------------------------------------------- |
| PCA                   | Linear technique for variance-based dimension reduction    |
| Principal Components  | Orthogonal directions capturing successively less variance |
| PC1 from Scatter Plot | Direction of max spread (longest data axis)                |
| PC2 from Scatter Plot | Perpendicular to PC1, next max spread                      |
| Projection            | $`Z = \tilde{X} V_k`$                                        |
| Interpretation        | Analyze eigenvector weights to contextualize components    |

---

##  Visual Insight (Optional)

For 2D data:

* PC1 aligns with the **long axis** of the ellipse formed by the scatter
* PC2 aligns with the **short axis**, orthogonal to PC1

---