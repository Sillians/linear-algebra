## **Orthogonal Matrices**

An **orthogonal matrix** is a square matrix whose columns (and rows) are orthonormal vectors.

---

## **Definition**

A matrix $Q$ is **orthogonal** if any of the following equivalent conditions hold:

* $`Q^\top Q = QQ^\top = I`$


* $`Q^{-1} = Q^\top`$


* $`\|Q\mathbf{x}\| = \|\mathbf{x}\|`$ for all vectors $`\mathbf{x}`$

---

## **Identifying Orthogonal Matrices**

To determine if a matrix $Q$ is orthogonal:

* Verify that $`Q^\top Q = I`$


* Check that its columns (or rows):

  * Are unit vectors: $`\|\mathbf{q}_i\| = 1`$
  * Are mutually orthogonal: $`\mathbf{q}_i^\top \mathbf{q}_j = 0`$ for $`i \ne j`$

**Example:**

If

$$
Q = \begin{bmatrix}
\frac{1}{\sqrt{2}} & \frac{1}{\sqrt{2}} \\
-\frac{1}{\sqrt{2}} & \frac{1}{\sqrt{2}}
\end{bmatrix}
$$

then

$$
Q^\top Q = I \Rightarrow Q \text{ is orthogonal.}
$$

---

## **Calculating the Inverse of an Orthogonal Matrix**

For an orthogonal matrix $Q$:

* $`Q^{-1} = Q^\top`$

The inverse is simply the transpose.

---

## **Calculating the Determinant of a Product of Matrices**

For square matrices $A$ and $B$ of the same size:

* $`\det(AB) = \det(A) \cdot \det(B)`$

For orthogonal matrices:

* $`\det(Q) = \pm 1`$


* If $`Q_1`$ and $`Q_2`$ are orthogonal:
  $`\det(Q_1 Q_2) = \det(Q_1) \cdot \det(Q_2)`$

---

## **Identifying True Statements About Orthogonal Matrices**

| Statement                                            | True/False |
| ---------------------------------------------------- | ---------- |
| The inverse of an orthogonal matrix is its transpose | ✅ True     |
| The determinant of an orthogonal matrix is always 1  | ❌ False    |
| The product of two orthogonal matrices is orthogonal | ✅ True     |
| All orthogonal matrices are symmetric                | ❌ False    |

---

## **Summary Table**

| Property       | Value        |
| -------------- | ------------ |
| $`Q^\top Q`$     | $I$          |
| $`Q^{-1}`$       | $`Q^\top`$     |
| $`\det(Q)`$      | $`+1`$ or $`-1`$ |
| Columns of $Q$ | Orthonormal  |

---

Orthogonal matrices are widely used in areas like **QR decomposition**, **rotations**, **reflections**, and **preserving vector lengths and angles**.
