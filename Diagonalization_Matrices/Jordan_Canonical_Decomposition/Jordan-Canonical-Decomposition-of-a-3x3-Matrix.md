## **Jordan Canonical Decomposition of a 3×3 Matrix**

---

### **I. Overview: Jordan Canonical Form**

The **Jordan Canonical Form** (JCF) of a square matrix $`A \in \mathbb{C}^{n \times n}`$ is a block-diagonal matrix $`J`$ such that:

$`A = PJP^{-1}`$

where:

* $`J`$ is composed of **Jordan blocks**, each corresponding to an eigenvalue.


* $`P`$ contains **generalized eigenvectors** of $`A`$.


Each **Jordan block** for eigenvalue $`\lambda`$ has the form:


$`J_k(\lambda) = \begin{bmatrix} \lambda & 1 & 0 & \cdots & 0 \\0 & \lambda & 1 & \cdots & 0 \\\vdots & \ddots & \ddots & \ddots & \vdots \\0 & \cdots & 0 & \lambda & 1 \\0 & \cdots & \cdots & 0 & \lambda \end{bmatrix}_{k \times k}`$


---

### **II. Jordan Decomposition of a 3×3 Matrix**

Let $`A \in \mathbb{C}^{3 \times 3}`$. The structure of $`J`$ and $`P`$ depends on the **algebraic and geometric multiplicities** of the eigenvalues of $A$.

---

### **III. Identifying the Columns of a Transformation Matrix $P$ in a Jordan Decomposition**

The columns of $`P`$ consist of:

* **Eigenvectors**, when geometric multiplicity = algebraic multiplicity.


* **Generalized eigenvectors**, when geometric multiplicity < algebraic multiplicity.


To construct $P$:

1. **For each Jordan block**:

   * If the block is size 1: choose an **eigenvector** $v$ such that $`(A - \lambda I)v = 0`$
   

   * If the block is size $> 1$: choose a **Jordan chain**:

     * For block of size 2: find $`v_1`$ such that $`(A - \lambda I)^2 v_1 = 0`$, $`(A - \lambda I)v_1 = v_2`$
     * Then columns of $P$ are $`v_2, v_1`$

---

### **IV. Finding a Jordan Decomposition of a 3×3 Matrix Given a Single Eigenvalue**

#### **Example:**

Let

$`A = \begin{bmatrix} 5 & 4 & 2 \\0 & 5 & 1 \\0 & 0 & 5 \end{bmatrix}`$

* Characteristic polynomial: $`(5 - \lambda)^3 \Rightarrow \lambda = 5`$, algebraic multiplicity 3


* Compute $`\ker(A - 5I)`$ → nullity = 1 → geometric multiplicity = 1


So, one Jordan block of size 3:

$`J = \begin{bmatrix} 5 & 1 & 0 \\0 & 5 & 1 \\0 & 0 & 5 \end{bmatrix}`$

**To find $`P`$:**

1. Find $`v \in \ker((A - 5I)^3) \setminus \ker((A - 5I)^2)`$


2. Construct chain: $`v_1, v_2, v_3`$ such that:


$`(A - 5I)v_1 = v_2, \quad (A - 5I)v_2 = v_3, \quad (A - 5I)v_3 = 0`$

Then:

$`P = [v_3 \; v_2 \; v_1]`$

---

### **V. Finding a Jordan Decomposition of a 3×3 Matrix Given Two Distinct Eigenvalues**

#### **Example:**

Let:

$`A = \begin{bmatrix} 2 & 1 & 0 \\0 & 2 & 0 \\0 & 0 & 3 \end{bmatrix}`$


* Eigenvalues: $`\lambda = 2`$ (algebraic multiplicity 2), $`\lambda = 3`$ (algebraic multiplicity 1)


* $`\ker(A - 2I)`$: dimension 1 → one Jordan block of size 2 for $`\lambda = 2`$


* $`\ker(A - 3I)`$: dimension 1 → one block of size 1 for $`\lambda = 3`$

So:

$`J = \begin{bmatrix} 2 & 1 & 0 \\0 & 2 & 0 \\0 & 0 & 3 \end{bmatrix}`$

**Constructing $P$:**

* For $`\lambda = 2`$:

  * Find $`v_1 \in \ker((A - 2I)^2) \setminus \ker(A - 2I)`$
  * Find $`v_2 = (A - 2I)v_1 \in \ker(A - 2I)`$


* For $`\lambda = 3`$:

  * Find eigenvector $`v_3 \in \ker(A - 3I)`$

Then:


$`P = [v_2 \; v_1 \; v_3]`$

---

### **VI. Summary Table**

| Case                          | Algebraic Multiplicity       | Geometric Multiplicity | Jordan Blocks                | Columns of $`P`$      |
| ----------------------------- | ---------------------------- | ---------------------- | ---------------------------- |-----------------------|
| Single eigenvalue             | 3                            | 1                      | One block size 3             | Generalized chain     |
| One eigenvalue, geom. mult. 2 | 3                            | 2                      | One block size 2, one size 1 | 2 chains              |
| Two distinct eigenvalues      | e.g., 2 (AM = 2), 3 (AM = 1) | e.g., 1, 1             | Block sizes 2, 1             | 1 chain + eigenvector |
| Three distinct eigenvalues    | 3                            | 3                      | Three blocks size 1          | 3 eigenvectors        |

---

### **VII. Key Steps in Practice**

1. **Compute Eigenvalues** of $A$


2. **Find Algebraic & Geometric Multiplicities**


3. **Determine Jordan Block Sizes**


4. **Find Eigenvectors and Generalized Eigenvectors**



5. **Assemble $J$ and construct $P$ from chains**

---
