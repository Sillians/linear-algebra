# **Linear Regression With Matrices**

Linear regression models the relationship between a dependent variable $`y`$ and one or more independent 
variables $`x`$ using a linear function. The matrix formulation is ideal for handling multiple variables and observations.

---

## **1. Linear Model in Matrix Form**

We express the model as:

$$
\mathbf{y} = X {\beta} + {\varepsilon}
$$

Where:

* $`\mathbf{y} \in \mathbb{R}^n`$: vector of observed outcomes
* $`X \in \mathbb{R}^{n \times p}`$: design matrix (each row is an observation, each column is a feature)
* $`{\beta} \in \mathbb{R}^p`$: vector of regression coefficients
* $`{\varepsilon} \in \mathbb{R}^n`$: vector of residuals (errors)

---

## **2. Least-Squares Estimate**

To find the best-fitting line, minimize the residual sum of squares:

$$
\min_{{\beta}} \| \mathbf{y} - X {\beta} \|^2
$$

This leads to the **normal equation**:

$$
\hat{{\beta}} = (X^\top X)^{-1} X^\top \mathbf{y}
$$

*(assuming $`X^\top X`$ is invertible)*

---

## **3. Predicted Values (Fitted Line)**

Once $`\hat{{\beta}}`$ is computed:

$$
\hat{\mathbf{y}} = X \hat{{\beta}}
$$

This gives the projection of $`\mathbf{y}`$ onto the column space of $`X`$.

---

## **4. Identifying Regression Elements From Matrix Terms**

In **simple linear regression**, the design matrix $`X`$ looks like:

$$
X = \begin{bmatrix}
1 & x_1 \\
1 & x_2 \\
\vdots & \vdots \\
1 & x_n
\end{bmatrix}, \quad
{\beta} =
\begin{bmatrix}
\beta_0 \\
\beta_1
\end{bmatrix}
$$

So, the fitted model becomes:

$$
\hat{\mathbf{y}} = \beta_0 \cdot \mathbf{1}_n + \beta_1 \cdot \mathbf{x}
$$


Which is the matrix version of:
$`\hat{y}\_i = \beta\_0 + \beta\_1 x\_i`$

---

## **5. Finding a Least-Squares Regression Line**

To compute $`\hat{{\beta}}`$:

1. Calculate $`X^\top X`$
2. Calculate $`X^\top \mathbf{y}`$
3. Solve:


$$
\hat{{\beta}} = (X^\top X)^{-1} X^\top \mathbf{y}
$$

---

## **6. Least-Squares Regression Line in Context**

Suppose you’re modeling **house prices** based on **square footage**.

* Let $`X`$ include a column of 1s and a column of square footage values.
* Solving for $`\hat{{\beta}}`$ gives:

  * $`\beta\_0`$: base price (intercept)
  * $`\beta\_1`$: price per square foot (slope)

The fitted line becomes:

$$
\text{Price} = \beta_0 + \beta_1 \cdot \text{SquareFootage}
$$

---

## **Summary Table**

| Concept        | Matrix Representation                  |
| -------------- | -------------------------------------- |
| Observations   | $`\mathbf{y}`$                         |
| Inputs         | $`X`$                                  |
| Coefficients   | $`{\beta}`$                            |
| Model Equation | $`\mathbf{y} = X{\beta} + {\varepsilon}`$ |
| Solution       | $`\hat{{\beta}} = (X^\top X)^{-1} X^\top \mathbf{y}`$ |
| Predictions    | $`\hat{\mathbf{y}} = X \hat{{\beta}}`$ |

---
