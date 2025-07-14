## **Projecting Vectors Onto Subspaces in Euclidean Spaces (Arbitrary Bases)**

---

### Overview

Projection of vectors onto subspaces allows decomposing a vector into components **along** and **orthogonal to** a given subspace. Unlike projections onto orthogonal bases, projection onto arbitrary bases involves solving systems using the **normal equations** or **matrix methods**.

---

### Key Concepts

| Concept             | Description                                                                 |
| ------------------- | --------------------------------------------------------------------------- |
| **Projection**      | The "shadow" or component of a vector that lies within a subspace.          |
| **Subspace**        | A subset of a vector space that is also a vector space (e.g., line, plane). |
| **Arbitrary Basis** | A spanning set of a subspace that may not be orthogonal or orthonormal.     |
| **Least Squares**   | The method used to find the closest vector in a subspace to a given vector. |

---

### General Formula (Arbitrary Basis)

Given a subspace $`W = \text{Col}(A)`$ where $A$ is an $`n \times k`$ matrix with **linearly independent columns**, and a vector $`b \in \mathbb{R}^n`$, 
the orthogonal projection of $`b`$ onto $`W`$ is:

$$
\text{proj}_W(b) = A(A^TA)^{-1}A^Tb
$$

This formula projects $b$ onto the column space of $A$.

---

### Applications and Deep Dives

#### Finding the Orthogonal Projection of a Vector Onto a Plane

Given a plane defined by two non-orthogonal vectors $`\vec{a}\_1, \vec{a}\_2`$, 
form matrix $`A = [\vec{a}\_1 \ \vec{a}\_2]`$ and use:

$$
\text{proj}_{\text{Plane}}(\vec{b}) = A(A^TA)^{-1}A^T \vec{b}
$$

This yields the closest point in the plane to $`\vec{b}`$.

---

#### Finding the Orthogonal Projection of a Vector Onto a Subspace

Given a subspace spanned by arbitrary basis vectors $`{ \vec{u}\_1, \dots, \vec{u}\_k }`$:

1. Construct matrix $`A = [\vec{u}\_1 \ \dots \ \vec{u}\_k]`$


2. Compute projection:

$$
\text{proj}_{\text{Subspace}}(\vec{v}) = A(A^TA)^{-1}A^T \vec{v}
$$

---

### Insight

Projections in arbitrary bases require solving a system due to a lack of orthogonality, 
but still reveal the **closest vector** in a subspace — a foundational idea 
behind **least-squares approximation**, **regression**, and **data compression**.

---

###  Summary

* Projections onto arbitrary subspaces use matrix projection: $`A(A^TA)^{-1}A^Tb`$.


* This technique generalizes projection when the basis is not orthogonal.


* Core to solving inconsistent systems, approximations, and optimization problems.

---
