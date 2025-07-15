### **Nilpotent and Idempotent Matrices, Deep Dive**

---

### **1. Overview**

In linear algebra, two special classes of square matrices with important algebraic properties are:

* **Nilpotent matrices**: Their powers eventually become the zero matrix.


* **Idempotent matrices**: Squaring them gives the same matrix back.

These structures show up in matrix decompositions, projections, and differential equations.

---

### **2. Nilpotent Matrices**

#### **Definition:**

A square matrix $`A \in \mathbb{R}^{n \times n}`$ is **nilpotent** if:

$`A^k = 0 \quad \text{for some smallest positive integer } k`$


* The **smallest such $k$** is called the **index of nilpotency**.


* All eigenvalues of a nilpotent matrix are 0.


#### **Example:**

$`A = \begin{bmatrix} 0 & 1 \\0 & 0 \end{bmatrix} \Rightarrow A^2 = \begin{bmatrix} 0 & 0 \\0 & 0 \end{bmatrix} \Rightarrow A \text{ is nilpotent of index 2}`$

---

### **3. Finding a Power of a Nilpotent Matrix**

If $A$ is nilpotent of index $k$, then:

* $`A^k = 0`$


* All higher powers also yield zero: $`A^m = 0`$ for $`m \geq k`$

#### **Example:**

Let

$`A = \begin{bmatrix} 0 & 1 & 0 \\0 & 0 & 1 \\0 & 0 & 0 \end{bmatrix} \Rightarrow A^3 = 0`$

So:

* $`A^1 = A`$


* $`A^2 \neq 0`$


* $`A^3 = 0`$

Hence, **index of nilpotency = 3**

---

### **4. Idempotent Matrices**

#### **Definition:**

A matrix $`P \in \mathbb{R}^{n \times n}`$ is **idempotent** if:

$$
P^2 = P
$$


* Idempotent matrices represent **projections** onto subspaces.


* Their eigenvalues are either 0 or 1.

#### **Example:**

$`P = \begin{bmatrix} 1 & 0 \\0 & 0 \end{bmatrix} \Rightarrow P^2 = P`$

✅ So, $P$ is idempotent.

---

### **5. Finding a Power of an Idempotent Matrix**

If $P$ is idempotent, then:

$`P^k = P \quad \text{for all } k \geq 1`$

So no matter how many times it's multiplied by itself, the result is always $P$.

#### **Example:**

$`P = \begin{bmatrix} 1 & 0 \\0 & 0 \end{bmatrix} \Rightarrow P^2 = P^3 = P^4 = \dots = P`$

---

### ✅ Summary Table

| Property          | Nilpotent Matrix                                 | Idempotent Matrix                              |
| ----------------- |--------------------------------------------------| ---------------------------------------------- |
| Definition        | $`A^k = 0`$ for some $k$                         | $`P^2 = P`$                                      |
| Eigenvalues       | All 0                                            | 0 or 1                                         |
| Powers            | $`A^k = 0`$, $`A^{k+1} = 0`$                     | $`P^k = P`$ for all $`k \geq 1`$                   |
| Example           | $`\begin{bmatrix} 0 & 1 \\ 0 & 0 \end{bmatrix}`$ | $`\begin{bmatrix} 1 & 0 \\ 0 & 0 \end{bmatrix}`$ |
| Geometric meaning | Collapse transformations                         | Projections onto subspaces                     |
| Application       | Jordan form, exponential series                  | Projections, least squares regression          |

---

These matrices play crucial roles in:

* The **Jordan canonical form** (nilpotent part)


* **Spectral theory**


* **Least squares** (idempotent projection matrices like the hat matrix $H$)


* **Matrix exponentials** for solving systems of differential equations.
