## **Orthogonal Matrix**

---

### **Definition**

A **matrix** $`Q \in \mathbb{R}^{n \times n}`$ is called an **orthogonal matrix** if its **transpose is equal to its inverse**:

$$
Q^T Q = QQ^T = I
$$

This means the **columns (and rows)** of $Q$ are:

* **Orthonormal vectors**, i.e.,

  * **Unit vectors**: each vector has norm 1
  * **Mutually orthogonal**: dot product between different vectors is 0

---

### **Mathematical Conditions**

For $`Q = [\mathbf{q}_1\ \mathbf{q}_2\ \cdots\ \mathbf{q}_n]`$, $Q$ is orthogonal if:

$$
\mathbf{q}_i \cdot \mathbf{q}_j =
\begin{cases}
1 & \text{if } i = j \\
0 & \text{if } i \neq j
\end{cases}
$$

---

### **Key Properties of Orthogonal Matrices**

| **Property**                       | **Explanation**                            |
| ---------------------------------- | ------------------------------------------ |
| $`Q^T = Q^{-1}`$                     | Inverse is its transpose                   |
| $`\det(Q) = \pm1`$                   | Preserves or flips orientation             |
| Preserves length                   | $`\|Q\mathbf{x}\| = \|\mathbf{x}\|`$         |
| Preserves angles                   | $`Q`$ is an isometry (distance-preserving)   |
| $Q$ represents rotation/reflection | Geometric interpretation in $`\mathbb{R}^n`$ |

---

### **Example**

Let:

$$
Q = \begin{bmatrix}
\frac{1}{\sqrt{2}} & \frac{1}{\sqrt{2}} \\
-\frac{1}{\sqrt{2}} & \frac{1}{\sqrt{2}}
\end{bmatrix}
$$

Then:

$$
Q^T Q = \begin{bmatrix}
\frac{1}{\sqrt{2}} & -\frac{1}{\sqrt{2}} \\
\frac{1}{\sqrt{2}} & \frac{1}{\sqrt{2}}
\end{bmatrix}
\begin{bmatrix}
\frac{1}{\sqrt{2}} & \frac{1}{\sqrt{2}} \\
-\frac{1}{\sqrt{2}} & \frac{1}{\sqrt{2}}
\end{bmatrix}
= \begin{bmatrix}
1 & 0 \\
0 & 1
\end{bmatrix} = I
$$

So $Q$ is orthogonal.

---

### **Geometric Insight**

Orthogonal matrices **preserve geometry**:

* **No stretching or skewing**
* **Just rotate or reflect**

This is critical in computer graphics, PCA, signal processing, and any field using orthonormal transformations.

---

### **Summary**

An orthogonal matrix:

* Has orthonormal columns (and rows)
* Satisfies $`Q^T = Q^{-1}`$
* Preserves vector lengths and angles
* Represents pure rotation or reflection in space

It's the algebraic form of "rigid transformations" in geometry.
