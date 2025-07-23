## **Reducing Real 2×2 Matrices to Rotation-Scaling Form**


A real $`2 \times 2`$ matrix can often be expressed in a simpler, more interpretable form—specifically 
as a combination of rotation and scaling. This is especially useful in geometric transformations and 
systems dynamics. The rotation-scaling form expresses a matrix $A$ as:


$`A = PDP^{-1}`$


where:

* $D$ is a diagonal or block-diagonal matrix with eigenvalues (may include complex conjugates),


* $P$ is a matrix of eigenvectors or generalized eigenvectors,


* and $A$ is interpreted as applying rotation (if complex eigenvalues) and/or scaling (if real eigenvalues).

---

### **Finding the Eigenvalues and Eigenvectors of a Matrix in Rotation-Scaling Form**

1. **Given a matrix** $`A = \begin{bmatrix} a & b \ c & d \end{bmatrix}`$, compute the **characteristic polynomial**:

$`\det(A - \lambda I) = \lambda^2 - \text{tr}(A)\lambda + \det(A)`$


2. **Solve for eigenvalues** $`\lambda\_1`$, $`\lambda\_2`$ (possibly complex).


3. For each eigenvalue, **solve** $`(A - \lambda I)\vec{v} = 0`$ to find the **eigenvectors**.


4. If eigenvalues are complex conjugates $`\lambda = \alpha \pm i\beta`$, then the matrix can be reduced to the form:


$`A = P \begin{bmatrix} \alpha & -\beta \\ \beta & \alpha \end{bmatrix} P^{-1}`$

---

### **Converting a Matrix to Rotation-Scaling Form Given Multiple Parts of the Decomposition**

If eigenvalues and eigenvectors are known:

* Construct $P$ using the eigenvectors as columns.


* Construct $D$ from eigenvalues.


* Verify that $`A = PDP^{-1}`$ holds.


* If eigenvectors are complex, use real matrices by converting $A$ to the form:


$`A = P \begin{bmatrix} \alpha & -\beta \\\beta & \alpha \end{bmatrix} P^{-1}`$


This block is called the **rotation-scaling** form.

---

### **Converting a Matrix to Rotation-Scaling Form Using the Complex Conjugate**

1. If eigenvalues are complex ($`\lambda = \alpha \pm i\beta`$), write the **real Jordan form** as:


$`J = \begin{bmatrix} \alpha & -\beta \\\beta & \alpha \end{bmatrix}`$


2. Choose a complex eigenvector $`\vec{v} = \vec{a} + i\vec{b}`$, then set:

$`P = [\vec{a}, \vec{b}]`$

so that:

$`A = PJP^{-1}`$


3. This decomposes $A$ into a combination of scaling (via $`\alpha`$) and rotation (via $`\beta`$).

---

### **Converting a Matrix to Rotation-Scaling Form Given Only One Eigenvalue**

If $A$ has a **repeated real eigenvalue** $`\lambda`$:

* Check whether $A$ is **diagonalizable**:

  * If yes: $`A = P \begin{bmatrix} \lambda & 0 \ 0 & \lambda \end{bmatrix} P^{-1} = \lambda I`$ (pure scaling).


* If no: Use **Jordan form**:


$`A = P \begin{bmatrix} \lambda & 1 \\ 0 & \lambda \end{bmatrix} P^{-1}`$


* This form still reflects scaling (through $`\lambda`$), but now with a **shear component**.

---

### Summary Table

| Matrix Type                 | Eigenvalues                   | Rotation-Scaling Form                                                                            |
| --------------------------- |-------------------------------|--------------------------------------------------------------------------------------------------|
| Diagonalizable real         | Real & distinct               | $`A = P D P^{-1\$, } D = diag(\$\lambda\_1, \lambda\_2`$)                                        |
| Complex eigenvalues         | $`\alpha \pm i\beta`$         | $`A = P \begin{bmatrix} \alpha & -\beta \ \beta & \alpha \end{bmatrix} P^{-1}`$                  |
| One real eigenvalue         | $`\lambda`$ (multiplicity 2)  | $`A = P \begin{bmatrix} \lambda & 1 \ 0 & \lambda \end{bmatrix} P^{-1}`$ (if not diagonalizable) |
| Scaling & rotation combined | Real + Complex eigenstructure | Captured in block-diagonal form of $J$                                                           |

This form is powerful in analyzing dynamics, especially when interpreting repeated applications of a linear transformation.
