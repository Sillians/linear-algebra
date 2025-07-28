## **QR Factorization**

---

### **1. Overview of QR Factorization**

**QR Factorization** expresses a matrix $`A \in \mathbb{R}^{m \times n}`$ as the product:

$`A = QR`$

Where:

* $`Q \in \mathbb{R}^{m \times n}`$ has **orthonormal columns** (i.e., $`Q^T Q = I_n`$)


* $`R \in \mathbb{R}^{n \times n}`$ is **upper triangular**


If $`m = n`$, then $`Q \in \mathbb{R}^{n \times n}`$ is an **orthogonal matrix** (i.e., $`Q^T Q = I_n = QQ^T`$)

QR factorization is commonly used in:

* Solving linear systems


* Least squares problems


* Eigenvalue algorithms


---

### **2. Identifying Dimensions of Factors in a QR Factorization**

Let $`A \in \mathbb{R}^{m \times n}`$ with **full column rank**:

| Matrix   | Dimensions       | Properties                               |
|----------|------------------|------------------------------------------|
| $`A`$    | $`m \times n`$   | Original matrix                          |
| $`Q`$    | $`m \times n`$   | Columns are orthonormal: $`Q^T Q = I_n`$ |
| $`R`$    | $`n \times n`$   | Upper triangular                         |

If $`A`$ is square (i.e., $`m = n`$), then $`Q \in \mathbb{R}^{n \times n}`$, $`R \in \mathbb{R}^{n \times n}`$

If $`A`$ is **tall** ($`m > n`$), then $`Q`$ has more rows than columns, and the QR factorization 
is sometimes extended to a **full QR** with $`Q \in \mathbb{R}^{m \times m}`$

---

### **3. Finding the Triangular Factor $`R`$ Given the Orthogonal Factor $`Q`$**

Given that $`A = QR`$ and $`Q`$ has orthonormal columns:

Multiply both sides by $`Q^T`$:

$`Q^T A = Q^T Q R = I R = R`$

**Therefore:**

$`R = Q^T A`$

So if $`Q`$ is known, compute $`R`$ by matrix multiplication.

---

### **4. Finding a QR Factorization Given an Orthogonal Basis for the Columns of a Matrix**

Suppose:

* $`A = [a_1 \ a_2 \ \dots \ a_n] \in \mathbb{R}^{m \times n}`$


* $`\{u_1, \dots, u_n\}`$ is an **orthonormal basis** of $`\mathrm{Col}(A)`$


* Write each $`a_k`$ as a linear combination of $`u_1, \dots, u_k`$

Then:

* Define $`Q = [u_1 \ \dots \ u_n]`$


* Let:

$`R_{ij} = \langle a_j, u_i \rangle, \quad \text{for } i \le j`$

* Then $`A = QR`$, where $`R`$ is upper triangular

---

### **5. Finding a QR Factorization Given a Matrix With Orthogonal Columns**

Suppose $`A \in \mathbb{R}^{m \times n}`$ has **orthogonal but not orthonormal** columns:

1. Normalize the columns of $A$:

$`Q = \left[ \frac{a_1}{\|a_1\|}, \dots, \frac{a_n}{\|a_n\|} \right]`$

2. Let:


$`R = \begin{bmatrix} \|a_1\| & 0 & \dots & 0 \\0 & \|a_2\| & \dots & 0 \\\vdots & \vdots & \ddots & \vdots \\0 & 0 & \dots & \|a_n\| \end{bmatrix}`$


3. Then $`A = QR`$

---

### **6. Finding the QR Factorization of a Matrix (Using Gram-Schmidt)**

Given a full-rank matrix $`A = [a_1, a_2, \dots, a_n] \in \mathbb{R}^{m \times n}`$:

Apply the **Gram-Schmidt process** to columns of $`A`$:

1. Initialize:

   * $`u_1 = a_1`$
   

   * $`q_1 = \frac{u_1}{\|u_1\|}`$


2. For $`k = 2`$ to $`n`$:

   * Subtract projections:

     $`u_k = a_k - \sum_{j=1}^{k-1} \langle a_k, q_j \rangle q_j`$

   * Normalize:

     $`q_k = \frac{u_k}{\|u_k\|}`$


3. Set $`Q = [q_1, \dots, q_n]`$


4. Compute $`R = Q^T A`$

---

### **7. Summary Table**

| Task                         | Formula / Procedure                                            |
|------------------------------|----------------------------------------------------------------|
| **QR Form**                  | $`A = QR`$                                                     |
| **Dimensions**               | $`Q: m \times n, \ R: n \times n`$                             |
| **Compute $`R`$ from $`Q`$** | $`R = Q^T A`$                                                  |
| **Given orthogonal basis**   | $`Q = [u_1, \dots, u_n], \ R_{ij} = \langle a_j, u_i \rangle`$ |
| **Given orthogonal columns** | Normalize columns for $`Q`$, place norms on diagonal of $`R`$  |
| **General process**          | Apply Gram-Schmidt to form $`Q`$, then $`R = Q^T A`$           |

---

