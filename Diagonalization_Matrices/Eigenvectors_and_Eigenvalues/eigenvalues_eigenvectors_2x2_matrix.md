## **Eigenvalues and Eigenvectors of a 2×2 Matrix**

---

### **1. What Are Eigenvalues and Eigenvectors?**

Given a square matrix $A$, a **non-zero vector** $\mathbf{v}$ is called an **eigenvector** of $A$ if:

$$
A\mathbf{v} = \lambda \mathbf{v}
$$

Where $\lambda$ is a **scalar** called the **eigenvalue** corresponding to eigenvector $\mathbf{v}$. This means applying the transformation $A$ to $\mathbf{v}$ only **stretches or shrinks** it—it doesn’t change its direction.

---

### **2. Finding Eigenvalues of a 2×2 Matrix**

Let:

$$
A = \begin{bmatrix}
a & b \\
c & d
\end{bmatrix}
$$

To find eigenvalues $\lambda$, solve the **characteristic equation**:

$$
\det(A - \lambda I) = 0
$$

Where $I$ is the identity matrix.

$$
A - \lambda I = \begin{bmatrix}
a - \lambda & b \\
c & d - \lambda
\end{bmatrix}
\Rightarrow
\det(A - \lambda I) = (a - \lambda)(d - \lambda) - bc = 0
$$

This is a quadratic in $\lambda$:

$$
\lambda^2 - (a + d)\lambda + (ad - bc) = 0
$$

---

### **3. Solving for Eigenvectors**

Once eigenvalues $\lambda_1, \lambda_2$ are found:

* Substitute each $\lambda$ into $(A - \lambda I)\mathbf{v} = 0$
* Solve the resulting system to get the **eigenvector(s)**

---

### **4. Example**

Let:

$$
A = \begin{bmatrix}
2 & 1 \\
1 & 2
\end{bmatrix}
$$

**Step 1: Characteristic Equation**

$$
\det(A - \lambda I) = \begin{vmatrix}
2 - \lambda & 1 \\
1 & 2 - \lambda
\end{vmatrix}
= (2 - \lambda)^2 - 1 = \lambda^2 - 4\lambda + 3 = 0
$$

$$
\Rightarrow \lambda = 1, 3
$$

**Step 2: Eigenvectors**

For $\lambda = 1$:

$$
A - I = \begin{bmatrix}
1 & 1 \\
1 & 1
\end{bmatrix}
\Rightarrow
\begin{bmatrix}
1 & 1 \\
1 & 1
\end{bmatrix}
\begin{bmatrix}
x \\
y
\end{bmatrix}
= 0
\Rightarrow x + y = 0 \Rightarrow \mathbf{v}_1 = \begin{bmatrix} 1 \\ -1 \end{bmatrix}
$$

For $\lambda = 3$:

$$
A - 3I = \begin{bmatrix}
-1 & 1 \\
1 & -1
\end{bmatrix}
\Rightarrow x - y = 0 \Rightarrow \mathbf{v}_2 = \begin{bmatrix} 1 \\ 1 \end{bmatrix}
$$

---

### **5. Summary**

For $`A = \begin{bmatrix} 2 & 1 \\ 1 & 2 \end{bmatrix}`$:

* **Eigenvalues:** $\lambda_1 = 1$, $\lambda_2 = 3$
* **Eigenvectors:**
  $`\mathbf{v}_1 = \begin{bmatrix} 1 \\ -1 \end{bmatrix}`$,
  $`\mathbf{v}_2 = \begin{bmatrix} 1 \\ 1 \end{bmatrix}`$

---

### **Key Insights**

* Eigenvectors reveal invariant directions of a transformation.
* Eigenvalues tell how much vectors are stretched or compressed.
* In ML and data science, they're used in PCA, spectral clustering, and more.


