## **Finding a Least-Squares Solution Using QR Factorization**

---

### **1. Overview of Least-Squares Problems**

In an **overdetermined** linear system $`A\mathbf{x} = \mathbf{b}`$ where $`A \in \mathbb{R}^{m \times n}`$ with $`m > n`$, 
an exact solution may not exist. Instead, we seek a **least-squares solution** $`\hat{\mathbf{x}} \in \mathbb{R}^n`$ that **minimizes the residual**:


$`\|\mathbf{b} - A\mathbf{x}\|_2`$


This is equivalent to projecting $`\mathbf{b}`$ orthogonally onto the **column space** of $`A`$, yielding:


$`A^T A \hat{\mathbf{x}} = A^T \mathbf{b}`$


Rather than solving this **normal equation**, which can be numerically unstable, we use **QR factorization** to compute $`\hat{\mathbf{x}}`$ more robustly.

---

### **2. QR Factorization and Least-Squares**

Let:

* $`A = QR`$, where:


  * $`Q \in \mathbb{R}^{m \times n}`$ has orthonormal columns (i.e., $`Q^T Q = I`$)


  * $`R \in \mathbb{R}^{n \times n}`$ is upper triangular


* $`\mathbf{b} \in \mathbb{R}^m`$

The least-squares solution is:


$`\hat{\mathbf{x}} = \arg\min_{\mathbf{x}} \|A\mathbf{x} - \mathbf{b}\| = \arg\min_{\mathbf{x}} \|QR\mathbf{x} - \mathbf{b}\|`$


Since $`Q`$ has orthonormal columns, multiply both sides by $`Q^T`$:


$`Q^T QR\mathbf{x} = Q^T \mathbf{b} \quad \Rightarrow \quad R\mathbf{x} = Q^T \mathbf{b}`$


Then:

* Solve the **upper triangular system** $`R\mathbf{x} = Q^T \mathbf{b}`$ for $`\hat{\mathbf{x}}`$

---

### **3. Expression for a Least-Squares Solution in Terms of Q and R**


Given $`A = QR`$, the least-squares solution to $`A\mathbf{x} = \mathbf{b}`$ is:


$`\boxed{ \hat{\mathbf{x}} = R^{-1} Q^T \mathbf{b} }`$


This assumes:

* $`Q \in \mathbb{R}^{m \times n}`$, $`R \in \mathbb{R}^{n \times n}`$, $`A`$ has full column rank


* $`Q^T \mathbf{b} \in \mathbb{R}^n`$


* Solve $`R \hat{\mathbf{x}} = Q^T \mathbf{b}`$ via back-substitution

---

### **4. Finding the Least-Squares Solution Given a QR Factorization**

#### **Given:**


* A matrix $`A \in \mathbb{R}^{m \times n}`$


* A vector $`\mathbf{b} \in \mathbb{R}^m`$


* QR factorization $`A = QR`$, with $`Q \in \mathbb{R}^{m \times n}`$, $`R \in \mathbb{R}^{n \times n}`$


#### **Steps:**

1. **Compute** $`\mathbf{y} = Q^T \mathbf{b} \in \mathbb{R}^n`$


2. **Solve** $`R \hat{\mathbf{x}} = \mathbf{y}`$ using back-substitution

---

### **5. Summary Table**

| Step  | Description                          | Expression                                   |
| ----- |--------------------------------------|----------------------------------------------|
| 1     | QR factorization                     | $`A = QR`$                                   |
| 2     | Project $`\mathbf{b}`$ onto Col$`A`$ | $`Q^T \mathbf{b}`$                           |
| 3     | Solve upper-triangular system        | $`R \hat{\mathbf{x}} = Q^T \mathbf{b}`$      |
| Final | Least-squares solution               | $`\hat{\mathbf{x}} = R^{-1} Q^T \mathbf{b}`$ |

---

### **6. Numerical Stability**

* Solving using QR is **more numerically stable** than solving $`A^T A \hat{\mathbf{x}} = A^T \mathbf{b}`$, especially for ill-conditioned matrices.


* QR avoids squaring the condition number of $`A`$, which happens in the normal equations.

---
