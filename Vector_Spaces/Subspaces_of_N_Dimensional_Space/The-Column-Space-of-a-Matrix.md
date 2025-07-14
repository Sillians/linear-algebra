## **The Column Space of a Matrix**

### **1. What Is the Column Space?**

The **column space** of a matrix $`A \in \mathbb{R}^{m \times n}`$, denoted $`\text{Col}(A)`$, 
is the set of all linear combinations of the columns of $A$:

$$
\text{Col}(A) = \text{Span}\{\vec{a}_1, \vec{a}_2, \ldots, \vec{a}_n\}
$$

where each $`\vec{a}_i \in \mathbb{R}^m`$ is a column vector of $A$.
It is a subspace of $`\mathbb{R}^m`$.

---

### **2. Determining if a Vector is in the Column Space of a Matrix**

To determine whether a vector $`\vec{b} \in \mathbb{R}^m`$ is in the column space of $A$, solve:

$$
A\vec{x} = \vec{b}
$$

* If a solution exists, then $`\vec{b} \in \text{Col}(A)`$.


* If there is no solution, then $`\vec{b} \notin \text{Col}(A)`$.

**Steps:**

1. Set up the augmented matrix $`[A \mid \vec{b}]`$


2. Use row-reduction (Gaussian elimination)


3. Check if the system is consistent

---

### **3. Determining the Value of an Unknown Given a Vector That’s in the Column Space of a Matrix**

Suppose a vector $`\vec{b}`$ contains a variable, and it's known that $`\vec{b} \in \text{Col}(A)`$. Then:

* Solve $`A\vec{x} = \vec{b}`$ symbolically.


* Determine the value(s) of the unknown that make the system consistent.


* Those are the values for which $`\vec{b}`$ lies in the column space.

---

### **4. Determining if a Vector Is in the Column Space of a Larger Matrix**

Even for larger matrices, the same principle holds:

$$
A\vec{x} = \vec{b}
$$

If the system has a solution, then $`\vec{b} \in \text{Col}(A)`$.
Use computational tools or matrix factorizations (e.g., QR decomposition) to assist in checking consistency efficiently for large matrices.

---

### **Summary**

* The column space is the span of the columns of a matrix.


* It consists of all vectors that can be written as $`A\vec{x}`$.


* A vector lies in the column space if the corresponding linear system is consistent.


* The **dimension** of the column space equals the **rank** of the matrix.

