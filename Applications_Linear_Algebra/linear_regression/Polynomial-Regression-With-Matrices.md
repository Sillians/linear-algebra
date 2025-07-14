## **Polynomial Regression With Matrices**

---

### **1. Overview: Polynomial Regression in Matrix Form**

Polynomial regression is a generalization of linear regression where the relationship between the 
independent variable $x$ and the dependent variable $y$ is modeled as an $n$-th degree polynomial:

$$
y = \beta_0 + \beta_1 x + \beta_2 x^2 + \dots + \beta_d x^d + \varepsilon
$$

Using matrices, this can be compactly expressed as:

$$
\mathbf{y} = X{\beta} + {\varepsilon}
$$

Where:

* $`\mathbf{y} \in \mathbb{R}^{m \times 1}`$: vector of observed outputs


* $`X \in \mathbb{R}^{m \times (d+1)}`$: **design matrix** (includes powers of $x$)


* $`{\beta} \in \mathbb{R}^{(d+1) \times 1}`$: vector of polynomial coefficients


* $`{\varepsilon} \in \mathbb{R}^{m \times 1}`$: residual vector

---

### **2. Finding an Expression for a Least-Squares Regression Curve**

Given a set of input-output data $`\{(x_i, y_i)\}_{i=1}^m`$, we fit a polynomial curve by minimizing the **sum of squared errors**:

$$
\min_{{\beta}} \| X{\beta} - \mathbf{y} \|^2
$$

This leads to the **normal equations**:

$$
X^\top X {\beta} = X^\top \mathbf{y}
$$

Solving this system yields the **least-squares solution**:

$$
{\beta} = (X^\top X)^{-1} X^\top \mathbf{y}
$$

Provided that $`X^\top X`$ is invertible (i.e., full rank).

---

### **3. Identifying the Elements of a Polynomial Regression Model**

For a polynomial of degree $d$, the model includes:

* **Independent variable terms:** $`x, x^2, \dots, x^d`$


* **Coefficients:** $`\beta_0, \beta_1, \dots, \beta_d`$


* **Intercept:** $`\beta_0`$


* **Design matrix rows:** For each data point $`x_i`$, the corresponding row in $X$ is:

$$
X_i = \begin{bmatrix} 1 & x_i & x_i^2 & \cdots & x_i^d \end{bmatrix}
$$

The complete design matrix $`X \in \mathbb{R}^{m \times (d+1)}`$ contains these rows stacked.

---

### **4. Identifying the Design Matrix When the Regression Curve Contains Zero Coefficients**

If a polynomial regression model omits certain powers of $x$ (i.e., their coefficients are known to be 0), the design matrix **must exclude those columns**.

**Example:**
Suppose the model is:

$$
y = \beta_0 + \beta_2 x^2 + \beta_3 x^3
$$

(No $`x^1`$ term; i.e., $`\beta_1 = 0`$)

Then for input data $`x_1, \dots, x_m`$, the design matrix is:

$$
X = \begin{bmatrix}
1 & x_1^2 & x_1^3 \\
1 & x_2^2 & x_2^3 \\
\vdots & \vdots & \vdots \\
1 & x_m^2 & x_m^3
\end{bmatrix}
\in \mathbb{R}^{m \times 3}
$$

**Important:** Columns corresponding to zero coefficients should be excluded **entirely** from $X$, not just zeroed out.

---

### **5. Summary Table: Polynomial Regression in Matrix Form**

| Component               | Symbol                                                   | Description           |
| ----------------------- | -------------------------------------------------------- | --------------------- |
| Response Vector         | $`\mathbf{y}`$                                             | Observed outputs      |
| Coefficient Vector      | $`{\beta}`$                                       | Polynomial parameters |
| Design Matrix           | $`X`$                                                      | Powers of input $x$   |
| Model Equation          | $`\mathbf{y} = X{\beta} + {\varepsilon}`$ | Regression equation   |
| Normal Equation         | $`X^\top X {\beta} = X^\top \mathbf{y}`$          | Solution condition    |
| Least Squares Estimator | $`{\beta} = (X^\top X)^{-1} X^\top \mathbf{y}`$   | Best fit              |

---

Polynomial regression using matrices offers a powerful and elegant way to model nonlinear data, 
and the matrix formulation makes it easy to implement, differentiate, 
and generalize — especially for machine learning and statistical computing.
