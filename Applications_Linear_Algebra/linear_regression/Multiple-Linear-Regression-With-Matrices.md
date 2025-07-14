## **Multiple Linear Regression With Matrices**

---

### **I. Overview of Multiple Linear Regression**

**Multiple Linear Regression** models the relationship between a dependent variable and multiple independent (predictor) variables. 
In matrix form, the model is expressed as:

$$
\mathbf{y} = X {\beta} + {\varepsilon}
$$

Where:

* $`mathbf{y} \in \mathbb{R}^{n}`$: vector of observed responses (dependent variable),
* $`X \in \mathbb{R}^{n \times p}`$: **design matrix** (rows are data points, columns are predictors),
* $`{\beta} \in \mathbb{R}^{p}`$: vector of unknown regression coefficients,
* $`{\varepsilon} \in \mathbb{R}^{n}`$: vector of random errors (assumed to be normally distributed with mean 0 and variance $`\sigma^2`$).

---

### **II. Least Squares Estimation**

The goal is to minimize the **residual sum of squares**:

$$
\min_{{\beta}} \|\mathbf{y} - X{\beta}\|^2
$$

This leads to the **normal equations**:

$$
X^\mathsf{T}X {\beta} = X^\mathsf{T} \mathbf{y}
$$

If $`X^\mathsf{T}X`$ is invertible, the least-squares solution is:

$$
{\beta} = (X^\mathsf{T}X)^{-1} X^\mathsf{T} \mathbf{y}
$$

---

### **III. Identifying Elements of a Multiple Linear Regression**

| Element                                           | Description                                                                          |
|---------------------------------------------------| ------------------------------------------------------------------------------------ |
| $`\mathbf{y}`$                                    | Response vector (length $n$)                                                         |
| $X$                                               | Design matrix (size $`n \times p`$); typically includes a column of 1s for the intercept |
| $`{\beta}`$                                       | Coefficient vector (length $p$)                                                      |
| $`\hat{\mathbf{y}} = X{\beta}`$                   | Fitted or predicted values                                                           |
| $`{\varepsilon} = \mathbf{y} - \hat{\mathbf{y}}`$ | Residuals (errors)                                                                   |

**Example Design Matrix with Intercept:**

$$
X =
\begin{bmatrix}
1 & x_{11} & x_{12} & \cdots & x_{1(p-1)} \\
1 & x_{21} & x_{22} & \cdots & x_{2(p-1)} \\
\vdots & \vdots & \vdots & \ddots & \vdots \\
1 & x_{n1} & x_{n2} & \cdots & x_{n(p-1)}
\end{bmatrix}
$$

* First column of 1s models the intercept.
* Remaining columns represent the predictors.

---

### **IV. Identifying Elements of a Multiple Linear Regression That Passes Through the Origin**

When the regression is **forced to pass through the origin**, there is **no intercept term**. The model becomes:

$$
\mathbf{y} = X {\beta} + {\varepsilon}
$$

Where:

* $X$ **does not contain** a column of 1s.
* The model assumes that when all predictors are 0, the response is 0.

**Modified Design Matrix:**

$$
X =
\begin{bmatrix}
x_{11} & x_{12} & \cdots & x_{1p} \\
x_{21} & x_{22} & \cdots & x_{2p} \\
\vdots & \vdots & \ddots & \vdots \\
x_{n1} & x_{n2} & \cdots & x_{np}
\end{bmatrix}
$$

| Element       | Without Intercept (Through Origin)        |
|---------------| ----------------------------------------- |
| $X$           | No leading column of 1s                   |
| $`{\beta}`$   | Only slopes                               |
| Model form    | $`\hat{\mathbf{y}} = X {\beta}`$ |

---

### **V. Geometric Interpretation**

* The least squares solution projects $`\mathbf{y}`$ **orthogonally** onto the column space of $X$.
* $`\hat{\mathbf{y}}`$ lies in $`\text{Col}(X)`$.
* The residual vector $`{\varepsilon} = \mathbf{y} - \hat{\mathbf{y}}`$ is orthogonal to every column of $X$.

---

### **VI. Summary**

| Concept             | Standard Regression                                        | Regression Through Origin     |
| ------------------- |------------------------------------------------------------|-------------------------------|
| Intercept Included? | Yes (column of 1s)                                         | No                            |
| Design Matrix $X$   | $`n \times p`$ (with 1s column)                            | $`n \times p`$ (no 1s column) |
| $`{\beta}`$ | Includes intercept                                         | Slopes only                   |
| Model Equation      | $`\mathbf{y} = X{\beta} + {\varepsilon}`$                  | Same form, different $X$      |

Multiple linear regression using matrices provides a concise and powerful framework for modeling, estimation, and interpretation — both with and without an intercept term.
