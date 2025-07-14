## **Orthogonal Linear Transformations — Deep Dive**

---

## **1. Definition**

A **linear transformation** $`T : \mathbb{R}^n \to \mathbb{R}^n`$ is called **orthogonal** if it **preserves the dot product**:

$$
\langle T(\mathbf{u}), T(\mathbf{v}) \rangle = \langle \mathbf{u}, \mathbf{v} \rangle \quad \forall \, \mathbf{u}, \mathbf{v} \in \mathbb{R}^n
$$

If $T$ is represented by a matrix $Q$, then:

$$
Q^T Q = Q Q^T = I_n
$$

Such transformations preserve both **lengths** and **angles**, including **rotations** and **reflections**.

---

## **2. Geometric Interpretation**

Orthogonal transformations:

* **Preserve lengths**:

$$
\|T(\mathbf{v})\| = \|\mathbf{v}\|
$$

* **Preserve angles**:

$$
\cos \theta = \frac{\langle \mathbf{u}, \mathbf{v} \rangle}{\|\mathbf{u}\| \|\mathbf{v}\|} = \frac{\langle T(\mathbf{u}), T(\mathbf{v}) \rangle}{\|T(\mathbf{u})\| \|T(\mathbf{v})\|}
$$

* **Preserve orthogonality**:

$$
\text{If } \mathbf{u} \perp \mathbf{v}, \text{ then } T(\mathbf{u}) \perp T(\mathbf{v})
$$

---

## **3. Matrix Representation and Properties**

If $`Q \in \mathbb{R}^{n \times n}`$ is an orthogonal matrix:

* $`Q^T Q = I_n`$


* $`Q^{-1} = Q^T`$


* Columns and rows of $Q$ form **orthonormal sets**


* $`\det(Q) = \pm 1`$

  * $`\det(Q) = +1`$ → rotation
  * $`\det(Q) = -1`$ → reflection

---

## **4. Applying the Angle Preserving Property**

Let $`\mathbf{u}, \mathbf{v} \in \mathbb{R}^n`$ and $T$ be orthogonal.

### **Steps**:

1. Compute angle between $`\mathbf{u}, \mathbf{v}`$:

$$
\cos \theta = \frac{\langle \mathbf{u}, \mathbf{v} \rangle}{\|\mathbf{u}\| \|\mathbf{v}\|}
$$


2. Apply transformation:

$$
T(\mathbf{u}), \quad T(\mathbf{v})
$$


3. Use:

$$
\cos \theta' = \frac{\langle T(\mathbf{u}), T(\mathbf{v}) \rangle}{\|T(\mathbf{u})\| \|T(\mathbf{v})\|} = \cos \theta
$$

Hence, the **angle is preserved** under $T$.

---

## **5. Identifying the Orthogonality of a Two-Vector Set**

Two vectors $`\mathbf{u}, \mathbf{v}`$ are **orthogonal** if:

$$
\langle \mathbf{u}, \mathbf{v} \rangle = 0
$$

### **Steps**:

1. Compute dot product:

$$
\mathbf{u} \cdot \mathbf{v} = \sum u_i v_i
$$

2. If the result is zero, then the vectors are orthogonal.

---

## **6. Example**

Let:

$$
Q = \begin{bmatrix}
\cos \theta & -\sin \theta \\
\sin \theta & \cos \theta
\end{bmatrix}
$$

This is a **2×2 rotation matrix**, and it satisfies:

$$
Q^T Q = I_2
$$

Let:

* $`\mathbf{u} = \begin{bmatrix}1 \\ 0\end{bmatrix}`$


* $`\mathbf{v} = \begin{bmatrix}0 \\ 1\end{bmatrix}`$

Then:

* $`\langle \mathbf{u}, \mathbf{v} \rangle = 0`$


* $`T(\mathbf{u}) = \begin{bmatrix} \cos \theta \\ \sin \theta \end{bmatrix}`$


* $`T(\mathbf{v}) = \begin{bmatrix} -\sin \theta \\ \cos \theta \end{bmatrix}`$

Check:

$$
\langle T(\mathbf{u}), T(\mathbf{v}) \rangle = \cos \theta (-\sin \theta) + \sin \theta \cos \theta = 0
$$

So, orthogonality is preserved.

---

##  Summary Table

| **Property**                 | **Orthogonal Transformation** |
| ---------------------------- | ----------------------------- |
| Length preserved             | ✅                             |
| Angle preserved              | ✅                             |
| Dot product preserved        | ✅                             |
| Matrix form                  | $`Q^T Q = I`$                   |
| Inverse                      | $`Q^{-1} = Q^T`$                |
| Determinant                  | $`\pm 1`$                       |
| Examples                     | Rotations, Reflections        |
| Columns form orthonormal set | ✅                             |

---
