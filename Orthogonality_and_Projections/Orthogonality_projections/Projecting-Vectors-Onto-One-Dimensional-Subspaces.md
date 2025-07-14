## **Projecting Vectors Onto One-Dimensional Subspaces**

---

### **1. Overview of Projection Onto a One-Dimensional Subspace**

A **projection** is the closest point (in Euclidean distance) on a subspace to a given vector. 
When projecting onto a **one-dimensional subspace**, this subspace is spanned by a single nonzero vector $`\mathbf{u}`$. 
The projection of a vector $`\mathbf{v}`$ onto the line through $`\mathbf{u}`$ is denoted:

$$
\text{proj}_{\mathbf{u}} \mathbf{v}
$$

---

### **2. Finding the Orthogonal Projection of a Vector onto a One-Dimensional Subspace**

Given a nonzero vector $`\mathbf{u} \in \mathbb{R}^n`$ and a vector $`\mathbf{v} \in \mathbb{R}^n`$, 
the orthogonal projection of $`\mathbf{v}`$ onto the line spanned by $`\mathbf{u}`$ is:

$$
\text{proj}_{\mathbf{u}} \mathbf{v} = \frac{\mathbf{v} \cdot \mathbf{u}}{\mathbf{u} \cdot \mathbf{u}} \mathbf{u}
$$

#### Notes:

* The result is a vector parallel to $`\mathbf{u}`$.


* The projection minimizes the distance from $`\mathbf{v}`$ to the subspace.

---

### **3. Calculating the Distance Between a Vector and a One-Dimensional Subspace**

The **distance** between $`\mathbf{v}`$ and the subspace spanned by $`\mathbf{u}`$ is the norm of the **rejection**, the component orthogonal to the subspace:

$$
\text{dist}(\mathbf{v}, \text{Span}\{\mathbf{u}\}) = \left\| \mathbf{v} - \text{proj}_{\mathbf{u}} \mathbf{v} \right\|
$$

This gives the shortest Euclidean distance from $`\mathbf{v}`$ to the subspace.

---

### **4. Finding the Orthogonal Projection of a Vector onto the Solution Space of a System of Equations**

Let the solution space of a homogeneous system $`A\mathbf{x} = \mathbf{0}`$ be a line spanned by vector $`\mathbf{u}`$. 
To project $`\mathbf{v}`$ onto this space:

1. **Find a basis** $`\{\mathbf{u}\}`$ for the solution space.


2. Use the projection formula:

$$
\text{proj}_{\text{N}(A)} \mathbf{v} = \frac{\mathbf{v} \cdot \mathbf{u}}{\mathbf{u} \cdot \mathbf{u}} \mathbf{u}
$$

This gives the projection of $`\mathbf{v}`$ onto the null space of $A$, assuming it's one-dimensional.

---

### **5. Summary Table**

| Task                                                         | Formula                                                                                                                          |
| ------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------- |
| Orthogonal projection of $`\mathbf{v}`$ onto $`\mathbf{u}`$      | $`\displaystyle \text{proj}_{\mathbf{u}} \mathbf{v} = \frac{\mathbf{v} \cdot \mathbf{u}}{\mathbf{u} \cdot \mathbf{u}} \mathbf{u}`$ |
| Distance from $`\mathbf{v}`$ to line $`\text{Span}(\mathbf{u})`$ | $`\left\| \mathbf{v} - \text{proj}_{\mathbf{u}} \mathbf{v} \right\|`$                                                              |
| Projection onto solution space of $`A\mathbf{x} = \mathbf{0}`$ | Same as projection onto a basis vector of $`\text{N}(A)`$                                                                          |

---

### **6. Geometric Intuition**

* The projection "drops a perpendicular" from $`\mathbf{v}`$ onto the subspace.


* The resulting vector lies **in the subspace** and represents the **closest approximation** of $`\mathbf{v}`$ within that space.


* The orthogonal component (error or residual) is perpendicular to the subspace.

---

### **Key Insight**

Projecting onto a one-dimensional subspace simplifies to scaling the direction vector $`\mathbf{u}`$ by 
how much $`\mathbf{v}`$ "aligns" with $`\mathbf{u}`$. This is foundational in approximation theory, least-squares problems, and signal decomposition.
