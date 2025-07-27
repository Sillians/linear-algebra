## **Projecting Vectors Onto Subspaces in Inner Product Spaces**

---

### **1. Overview**

In an inner product space $`V`$, the **orthogonal projection** of a vector $`v`$ onto a subspace $`W \subseteq V`$ 
is the unique vector $`\hat{v} \in W`$ such that the difference $`v - \hat{v}`$ is **orthogonal** to all 
vectors in $`W`$.

Formally:


* If $`\hat{v} \in W`$, then $`v - \hat{v} \in W^\perp`$


* The projection minimizes the distance $`\|v - w\|`$ for all $`w \in W`$

---

### **2. Orthogonal Projection Onto a One-Dimensional Subspace**

Let:

* $`v \in V`$


* $`u \in V`$, $`u \ne 0`$, spans the subspace $`W = \mathrm{Span}\{u\}`$


Then the **orthogonal projection** of $`v`$ onto $`W`$ is:


$`\mathrm{proj}_u(v) = \frac{\langle v, u \rangle}{\langle u, u \rangle} u`$

Where:

* $`\langle \cdot , \cdot \rangle`$ is the inner product


* This yields the closest vector in the subspace $`\mathrm{Span}\{u\}`$

---

### **3. Orthogonal Projection Onto a Subspace Spanned by Orthogonal Vectors**

Let:

* $`v \in V`$


* $`\{u_1, u_2, \dots, u_k\} \subseteq V`$ be an **orthogonal set**


* Let $`W = \mathrm{Span}\{u_1, \dots, u_k\}`$


Then:

$`\mathrm{proj}_W(v) = \sum_{i=1}^k \frac{\langle v, u_i \rangle}{\langle u_i, u_i \rangle} u_i`$

If the set is **orthonormal** (i.e., $`\|u_i\| = 1`$), this simplifies to:


$`\mathrm{proj}_W(v) = \sum_{i=1}^k \langle v, u_i \rangle u_i`$


This generalizes the one-dimensional case and is extremely useful when working with bases like Fourier or Legendre polynomials.

---

### **4. Calculating the Distance Between a Vector and a Subspace**

Let:

* $`v \in V`$


* $`W \subseteq V`$ be a subspace


* $`\hat{v} = \mathrm{proj}_W(v)`$


Then the **distance** between $`v`$ and the subspace $`W`$ is:


$`\mathrm{dist}(v, W) = \|v - \hat{v}\| = \|v - \mathrm{proj}_W(v)\|`$


In normed inner product spaces, this gives the length of the **orthogonal component** of $`v`$ with respect to $`W`$.

---

### **5. Summary Table**

| Task                                          | Formula                                                                                    |
|-----------------------------------------------|--------------------------------------------------------------------------------------------|
| Projection onto $`\mathrm{Span}\{u\}`$        | $`\displaystyle \mathrm{proj}_u(v) = \frac{\langle v, u \rangle}{\langle u, u \rangle} u`$ |
| Projection onto orthogonal basis $`\{u_i\}`$  | $`\displaystyle \sum_{i=1}^k \frac{\langle v, u_i \rangle}{\langle u_i, u_i \rangle} u_i`$ |
| Projection onto orthonormal basis $`\{u_i\}`$ | $`\displaystyle \sum_{i=1}^k \langle v, u_i \rangle u_i`$                                  |
| Distance from $`v`$ to subspace $`W`$         | $`\displaystyle \|v - \mathrm{proj}_W(v)\|`$                                               |

---

### **6. Important Notes**

* Orthogonal projections are **linear transformations**.
* They satisfy $`\mathrm{proj}_W^2 = \mathrm{proj}_W`$ and are **idempotent**.
* They decompose vectors as:

$`v = \mathrm{proj}_W(v) + (v - \mathrm{proj}_W(v)) \in W \oplus W^\perp`$

---