## **Finding Generalized Eigenvectors of Specific Ranks**

---

## **1. Generalized Eigenvectors: Definition**

Let $`A \in \mathbb{C}^{n \times n}`$ (or $`\mathbb{R}^{n \times n}`$), and let $`\lambda`$ be an eigenvalue 
of $`A`$. A **generalized eigenvector of rank $`k`$** is a nonzero vector $`\mathbf{v} \in \mathbb{C}^n`$ 
such that:


* $`(A - \lambda I)^k \mathbf{v} = 0`$


* $`(A - \lambda I)^{k-1} \mathbf{v} \ne 0`$


The smallest such $`k \geq 1`$ is called the **rank** or **order** of the generalized eigenvector.

---

## **2. Role of Generalized Eigenvectors**

* They arise when the matrix is **not diagonalizable**, i.e., when the geometric multiplicity of an eigenvalue is **less than** its algebraic multiplicity.


* Generalized eigenvectors are used to form a **Jordan basis** and express the matrix in **Jordan canonical form**.


* The length of a Jordan block equals the **rank of the highest generalized eigenvector** in its chain.

---

## **3. Algorithm to Find Generalized Eigenvectors**

Given matrix $`A`$ and eigenvalue $`\lambda`$:

1. Compute $`A - \lambda I`$.


2. Find null spaces of increasing powers:
   $`\mathcal{N}_1 = \ker(A - \lambda I), \mathcal{N}_2 = \ker((A - \lambda I)^2), \dots`$


3. For rank-$`k`$ generalized eigenvectors, find $`\mathbf{v} \in \mathcal{N}_k \setminus \mathcal{N}_{k-1}`$.


4. Build Jordan chains:

$`\mathbf{v}_k,\, (A - \lambda I)\mathbf{v}_k = \mathbf{v}_{k-1},\, \dots,\, (A - \lambda I)^{k-1} \mathbf{v}_k = \mathbf{v}_1 \in \ker(A - \lambda I)`$

---

## **4. Example: 2×2 Matrix**

### **Matrix**

$`A = \begin{bmatrix} 2 & 1 \\ 0 & 2 \end{bmatrix}`$

### **Eigenvalue**

$`\lambda = 2,\quad \text{algebraic multiplicity} = 2`$


$`A - 2I = \begin{bmatrix} 0 & 1 \\ 0 & 0 \end{bmatrix} \Rightarrow \ker(A - 2I) = \mathrm{span} \left\{ \begin{bmatrix} 1 \\ 0 \end{bmatrix} \right\}`$

Only 1 eigenvector → $A$ is not diagonalizable.

### **Generalized Eigenvector**

Want $`\mathbf{v}`$ such that:

* $`(A - 2I)^2 \mathbf{v} = 0`$


* $`(A - 2I) \mathbf{v} \ne 0`$

Try $`\mathbf{v} = \begin{bmatrix} 0 \\ 1 \end{bmatrix}`$:


$`(A - 2I)\mathbf{v} = \begin{bmatrix} 1 \\ 0 \end{bmatrix} \ne 0,\quad(A - 2I)^2 \mathbf{v} = 0`$


✅ So $`\mathbf{v} = \begin{bmatrix} 0 \\ 1 \end{bmatrix}`$ is a **rank-2 generalized eigenvector**

---

## **5. Example: 3×3 Matrix**

### **Matrix**


$`A = \begin{bmatrix} 5 & 1 & 0 \\0 & 5 & 1 \\0 & 0 & 5 \end{bmatrix}`$


This is a **Jordan block $`J_3(5)`$**.


### **Eigenvalue**

$`\lambda = 5,\quad \text{algebraic multiplicity} = 3`$

$`A - 5I = \begin{bmatrix} 0 & 1 & 0 \\0 & 0 & 1 \\0 & 0 & 0 \end{bmatrix} \Rightarrow \ker(A - 5I) = \mathrm{span} \left\{ \begin{bmatrix} 1 \\ 0 \\ 0 \end{bmatrix} \right\}`$

### **Generalized Eigenvector of Rank 3**

Let $`\mathbf{v}_3 = \begin{bmatrix} 0 \\ 0 \\ 1 \end{bmatrix}`$, then:


$`(A - 5I)\mathbf{v}_3 = \begin{bmatrix} 0 \\ 1 \\ 0 \end{bmatrix} \quad (\mathbf{v}_2)\\(A - 5I)\mathbf{v}_2 = \begin{bmatrix} 1 \\ 0 \\ 0 \end{bmatrix} \quad (\mathbf{v}_1)\\(A - 5I)\mathbf{v}_1 = 0`$

✅ $`\mathbf{v}_3`$ is a **rank-3 generalized eigenvector**

Jordan chain:

$`\mathbf{v}_3 = \begin{bmatrix} 0 \\ 0 \\ 1 \end{bmatrix},\; \mathbf{v}_2 = \begin{bmatrix} 0 \\ 1 \\ 0 \end{bmatrix},\; \mathbf{v}_1 = \begin{bmatrix} 1 \\ 0 \\ 0 \end{bmatrix}`$

---

## **6. Example: 4×4 Matrix**

### **Matrix**

$`A = \begin{bmatrix} 3 & 1 & 0 & 0 \\0 & 3 & 1 & 0 \\0 & 0 & 3 & 1 \\0 & 0 & 0 & 3 \end{bmatrix}`$

This is a **Jordan block $`J_4(3)`$**.


### **Eigenvalue**

$`\lambda = 3,\quad \text{algebraic multiplicity} = 4`$


$`A - 3I = \begin{bmatrix} 0 & 1 & 0 & 0 \\0 & 0 & 1 & 0 \\0 & 0 & 0 & 1 \\0 & 0 & 0 & 0 \end{bmatrix}`$


### **Generalized Eigenvector of Rank 4**

Let $`\mathbf{v}_4 = \begin{bmatrix} 0 \\ 0 \\ 0 \\ 1 \end{bmatrix}`$


Compute chain:

* $`\mathbf{v}_3 = (A - 3I)\mathbf{v}_4 = \begin{bmatrix} 0 \\ 0 \\ 1 \\ 0 \end{bmatrix}`$


* $`\mathbf{v}_2 = (A - 3I)\mathbf{v}_3 = \begin{bmatrix} 0 \\ 1 \\ 0 \\ 0 \end{bmatrix}`$


* $`\mathbf{v}_1 = (A - 3I)\mathbf{v}_2 = \begin{bmatrix} 1 \\ 0 \\ 0 \\ 0 \end{bmatrix}`$


* $`(A - 3I)\mathbf{v}_1 = 0`$

✅ $`\mathbf{v}_4`$ is a **rank-4 generalized eigenvector**

---

## **7. Summary Table**

| Matrix | Eigenvalue | Algebraic Multiplicity | Geometric Multiplicity | Rank | Generalized Eigenvector                          |
| ------ | ---------- | ---------------------- | ---------------------- | ---- | ------------------------------------------------ |
| 2×2    | 2          | 2                      | 1                      | 2    | $`\begin{bmatrix} 0 \\ 1 \end{bmatrix}`$           |
| 3×3    | 5          | 3                      | 1                      | 3    | $`\begin{bmatrix} 0 \\ 0 \\ 1 \end{bmatrix}`$      |
| 4×4    | 3          | 4                      | 1                      | 4    | $`\begin{bmatrix} 0 \\ 0 \\ 0 \\ 1 \end{bmatrix}`$ |

---

## **8. Conclusion**

* Generalized eigenvectors allow full decomposition of non-diagonalizable matrices.


* They are critical for forming the **Jordan canonical form**.


* The **rank** corresponds to the **size of the Jordan block**.


* Computing them involves analyzing successive null spaces of $`(A - \lambda I)^k`$.

This framework generalizes to higher dimensions and more complex Jordan structures.
