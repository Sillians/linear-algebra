# **Projecting Vectors Onto Subspaces in Euclidean Spaces**

---

## **1. Overview**

Projecting a vector onto a **subspace** in Euclidean space helps:

* Simplify problems


* Minimize distances


* Solve constrained optimization problems

Given a subspace $`W \subseteq \mathbb{R}^n`$ and a vector $`\mathbf{v} \in \mathbb{R}^n`$, we seek:

* The **orthogonal projection** of $`\mathbf{v}`$ onto $W$


* The **component of $`\mathbf{v}`$ orthogonal to $W$**

---

## **2. Projection Onto a Subspace With Arbitrary Basis**

Let $W$ be a subspace with basis vectors $`\{\mathbf{w}_1, \dots, \mathbf{w}_k\}`$.

### **Step 1: Form the Matrix**

Let $`A = [\mathbf{w}_1 \ \mathbf{w}_2 \ \dots \ \mathbf{w}_k] \in \mathbb{R}^{n \times k}`$.

---

### **Step 2: Use the Projection Formula**

The **orthogonal projection** of $`\mathbf{v}`$ onto $W$ is:

$$
\mathrm{proj}_W(\mathbf{v}) = A (A^T A)^{-1} A^T \mathbf{v}
$$

This works for **any set of linearly independent basis vectors**.

---

## **3. Calculating the Distance Between a Vector and a Subspace**

Let:

* $`\mathbf{v}`$ be a vector in $`\mathbb{R}^n`$


* $`\hat{\mathbf{v}} = \mathrm{proj}_W(\mathbf{v})`$ be the projection

Then the **distance** is:

$$
\text{dist}(\mathbf{v}, W) = \|\mathbf{v} - \hat{\mathbf{v}}\|
$$

Where $`\|\cdot\|`$ denotes the Euclidean norm.

---

## **4. Calculating the Acute Angle Between a Vector and a Subspace**

Let:

* $\hat{\mathbf{v}} = \mathrm{proj}_W(\mathbf{v})$


* $\theta$ be the angle between $\mathbf{v}$ and $W$

Then:

$$
\cos \theta = \frac{\langle \mathbf{v}, \hat{\mathbf{v}} \rangle}{\|\mathbf{v}\| \|\hat{\mathbf{v}}\|}
$$

And:

$$
\theta = \cos^{-1} \left( \frac{\langle \mathbf{v}, \hat{\mathbf{v}} \rangle}{\|\mathbf{v}\| \|\hat{\mathbf{v}}\|} \right)
$$

---

## **5. Finding the Orthogonal Projection Onto the Solution Space of a Linear System**

Let:

* The solution space of $`A\mathbf{x} = 0`$ be a subspace $`W`$


* The **null space** of $`A`$ is the set of all vectors satisfying the equation

### **Steps**:

1. Find a basis $`\{\mathbf{n}_1, \dots, \mathbf{n}_k\}`$ for $`\text{Null}(A)`$


2. Form matrix $`N = [\mathbf{n}_1 \ \dots \ \mathbf{n}_k]`$


3. Use the projection formula:

$$
\mathrm{proj}_{\text{Null}(A)}(\mathbf{v}) = N(N^T N)^{-1} N^T \mathbf{v}
$$

This gives the component of $`\mathbf{v}`$ that lies in the solution space of the system.

---

## Summary Table

| **Concept**                            | **Formula / Interpretation**                                                                                        |
| -------------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| Projection onto arbitrary subspace     | $`\mathrm{proj}_W(\mathbf{v}) = A(A^T A)^{-1} A^T \mathbf{v}`$                                                        |
| Distance from vector to subspace       | $`\|\mathbf{v} - \mathrm{proj}_W(\mathbf{v})\|`$                                                                      |
| Angle between vector and subspace      | $`\cos^{-1} \left( \frac{\langle \mathbf{v}, \hat{\mathbf{v}} \rangle}{\|\mathbf{v}\| \|\hat{\mathbf{v}}\|} \right)`$ |
| Projection onto null space of a system | $`N(N^T N)^{-1} N^T \mathbf{v}`$                                                                                      |

---
