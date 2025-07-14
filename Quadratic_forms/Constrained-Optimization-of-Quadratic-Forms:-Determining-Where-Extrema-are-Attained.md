# **Constrained Optimization of Quadratic Forms**

*How and where do quadratic forms achieve their maximum or minimum when restricted to geometric constraints?*

A **quadratic form** in $`\mathbb{R}^n`$ is

$$
Q(\mathbf{x}) \;=\; \mathbf{x}^\mathsf{T}A\mathbf{x},
$$

where $A$ is an $`n\times n`$ symmetric matrix.  Because $A$ is symmetric, it admits an orthonormal eigenbasis with real eigen-values.  
Under most common constraints (circle, sphere, ellipse, ellipsoid) the extrema of $Q$ are completely governed by those eigen-values.

---

## 1 Eigen-value principle (Rayleigh quotient)

For any non-zero \$\mathbf{x}\in\mathbb R^n\$ define its **Rayleigh quotient**

$$
\rho(\mathbf{x})=\frac{\mathbf{x}^\mathsf{T}A\mathbf{x}}{\mathbf{x}^\mathsf{T}\mathbf{x}}.
$$

If the eigenvalues of $A$ are ordered $`\lambda\_{\min}\le\ldots\le\lambda\_{\max}`$ then

$$
\lambda_{\min}\;\le\;\rho(\mathbf{x})\;\le\;\lambda_{\max}\qquad\forall\,\mathbf{x}\ne \mathbf{0},
$$

and

* $`\rho(\mathbf{x})=\lambda\_{\max}`$ only when $`\mathbf{x}`$ is any eigenvector for $`\lambda\_{\max}`$.


* $`\rho(\mathbf{x})=\lambda\_{\min}`$ only when $`\mathbf{x}`$ is any eigenvector for $`\lambda\_{\min}`$.


Because many geometric constraints can be rewritten as $`\lVert\mathbf x\rVert=`$ 
constant (or an affine equivalent), extrema almost always occur along eigen-directions.

---

## 2 Finding extrema on the **unit circle** ($n=2$)

### Problem

Given

$$
Q(x,y)=\begin{bmatrix}x&y\end{bmatrix}
\begin{bmatrix}a&b\\ b&c\end{bmatrix}
\begin{bmatrix}x\\y\end{bmatrix},
\qquad
\text{subject to } x^2+y^2=1,
$$

find where $Q$ attains its maximum and minimum.

### Solution sketch

1. **Diagonalize** $A$: find eigenvalues $`\lambda\_1,\lambda\_2`$ ($`\lambda\_1\le\lambda\_2`$) with orthonormal eigenvectors $`\mathbf{v}\_1,\mathbf{v}\_2`$.


3. Any point on the unit circle may be expressed as


$$
\mathbf{x}=t\,\mathbf{v}_1+\sqrt{1-t^2}\,\mathbf{v}_2,\quad -1\le t\le 1.
$$


3. Then

$$
Q(\mathbf{x})=\lambda_1t^2+\lambda_2(1-t^2)
=\lambda_2+t^2(\lambda_1-\lambda_2).
$$

   * If $`\lambda\_1<\lambda\_2`$ the maximum occurs at $`|t|=0`$ (vector $`\mathbf{v}\_2`$) and the minimum at $`|t|=1`$ (vector $`\mathbf{v}\_1`$).
   * If $`\lambda\_1=\lambda\_2`$ the form is isotropic; every direction yields the same value.


### Take-away

*Max* $`= \lambda\_{\max}`$ at eigenvector of $`\lambda\_{\max}`$,


*Min* $`= \lambda\_{\min}`$ at eigenvector of $`\lambda\_{\min}`$.

---

## 3 Finding extrema on the **unit sphere** ($`\lVert\mathbf x\rVert=1`$ in $`\mathbb{R}^n`$)

### Method 1 – Rayleigh quotient

Directly apply the eigen-value principle:

$$
\max_{\lVert\mathbf{x}\rVert=1} Q(\mathbf{x}) = \lambda_{\max},\quad
\min_{\lVert\mathbf{x}\rVert=1} Q(\mathbf{x}) = \lambda_{\min}.
$$

Extrema occur **exactly** at eigenvectors for the largest and smallest eigen-values.

### Method 2 – Lagrange multipliers

Set

$$
\mathcal{L}(\mathbf{x},\lambda)=\mathbf{x}^\mathsf{T}A\mathbf{x}-\lambda(\mathbf{x}^\mathsf T\mathbf{x}-1).
$$

$$\nabla\_{\mathbf{x}}\mathcal{L}=2A\mathbf{x}-2\lambda\mathbf{x}=0
\iff A\mathbf{x}=\lambda\mathbf{x}$$, i.e., $`\mathbf{x}`$ is an eigenvector. The multiplier $`\lambda`$ equals the corresponding eigenvalue, reproducing the Rayleigh result.

---

## 4 Finding extrema over an **ellipse** (2-D) or **ellipsoid** (3-D)

### Example in $`\mathbb R^2`$

Ellipse constraint $`x^2/4 + y^2=1`$ ⇒ scaling matrix $`B=\\mathrm{diag}(2,1)`$, so let $`\mathbf{u}=B^{-1}\mathbf{x}`$ to map the ellipse to the unit circle.  Then

$$
Q(\mathbf{x})=\mathbf{x}^\mathsf{T}A\mathbf{x}
=\mathbf{u}^\mathsf{T}(B^\mathsf{T}AB)\,\mathbf{u},
\qquad \lVert\mathbf{u}\rVert=1.
$$

Thus **replace** $`A`$ by $`\tilde A=B^\mathsf TAB`$ and proceed exactly as in the unit-circle case.  Eigenvectors of $`\tilde A`$ map back to $`\mathbf{x}=B\mathbf{u}`$ on the original ellipse.

### General ellipsoid $`\mathbf{x}^\mathsf{T}C^{-1}\mathbf{x}=1`$

Similarly set $`\mathbf{u}=C^{-1/2}\mathbf{x}`$ to reduce the constraint to a sphere, optimize with matrix $`\tilde A=C^{-1/2}AC^{-1/2}`$, then map back.

---

## 5 Finding points where tangent-plane directions matter

Sometimes we want **directions** rather than points:

*If $A$ is positive-definite, $Q$ has only a global minimum at $`\mathbf{0}`$ unconstrained; under norm constraints, eigen-directions are always optimal.*

Conversely, if \$A\$ has both positive and negative eigen-values, level sets of \$Q\$ are hyperboloids and the unit sphere will intersect them along closed curves; eigenvectors again mark the extreme intersection points.

---

## 6 Algorithm (cheat-sheet)

1. **Write** the quadratic form $`Q(\mathbf{x})=\mathbf{x}^\mathsf{T}A\mathbf{x}`$; ensure $`A=A^\mathsf T`$.


3. **Identify constraint**

   * Unit sphere/circle? → set $`\lVert\mathbf x\rVert=1`$.
   * Ellipsoid/ellipse? → transform to sphere.
   

3. **Compute eigenvalues** $`\lambda\_1\le\dots\le\lambda\_n`$ and **orthonormal eigenvectors** $`{\mathbf v\_i}`$ of:

   * $A$ for sphere;
   * $`\tilde A = C^{-1/2}AC^{-1/2}`$ for ellipsoid.


4. **Extrema**

   * **Max** $`=\lambda\_{\max}`$ at $`\mathbf x\parallel\mathbf v\_{\max}`$.
   * **Min** $`=\lambda\_{\min}`$ at $`\mathbf x\parallel\mathbf v\_{\min}`$.

---

### Worked micro-example on an ellipse

> **Form** $`Q(x,y)=5x^2+6xy+2y^2`$

> **Constraint** $`x^2+4y^2=1`$.


*Scaling matrix* $$B=\\mathrm{diag}(1,2)\Rightarrow \tilde A=B^\mathsf{T}AB=
\begin{bmatrix}5&6\\6&32\end{bmatrix}$$.


Eigenvalues of $`\tilde A`$ are $`\lambda\_{1}\approx4`$, $`\lambda\_{2}\approx33`$.

*Therefore*

* Minimum $=4$ at $`\mathbf{u}=\mathbf{v}\_1`$, so $`\mathbf{x}=B\mathbf{u}`$ gives the ellipse point of minimum.


* Maximum $`=33`$ analogously.

---

### Key Takeaways

* Constrained quadratic optimization **boils down** to an eigen-problem.


* On norm-type constraints (circle, sphere) the extreme values **are exactly the extreme eigen-values**.


* On ellipses/ellipsoids, first map to a unit sphere to reuse the same principle.

With these tools you can locate extrema and the specific points (or directions) where they occur for *any* symmetric quadratic form under the most common geometric constraints.
