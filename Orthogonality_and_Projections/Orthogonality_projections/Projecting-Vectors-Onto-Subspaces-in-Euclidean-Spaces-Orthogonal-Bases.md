## **Projecting Vectors Onto Subspaces in Euclidean Spaces (Orthogonal Bases)**

Orthogonal projections are a way of expressing a vector in terms of components that lie within a given 
subspace and those that are orthogonal to it. If the subspace has an **orthogonal** or **orthonormal basis**, 
projections are especially efficient to compute.

---

## **1. Orthogonal Projection onto a Subspace Spanned by Orthogonal Vectors**

Given a subspace $W$ of $`\mathbb{R}^n`$ spanned by orthogonal vectors $`\mathbf{u}_1, \mathbf{u}_2, \dots, \mathbf{u}_k`$, and a vector $`\mathbf{v} \in \mathbb{R}^n`$, 
the **orthogonal projection** of $`\mathbf{v}`$ onto $W$ is:

$`\text{proj}_W(\mathbf{v}) = \sum_{i=1}^k \frac{\mathbf{v} \cdot \mathbf{u}_i}{\|\mathbf{u}_i\|^2} \mathbf{u}_i`$


If the vectors are orthonormal (i.e., $`\|\mathbf{u}_i\| = 1`$), this simplifies to:


$`\text{proj}_W(\mathbf{v}) = \sum_{i=1}^k (\mathbf{v} \cdot \mathbf{u}_i) \mathbf{u}_i`$

---

## **2. Finding the Orthogonal Projection of a Vector Onto a Plane**

Let the plane be spanned by two **orthogonal** vectors $`\mathbf{u}_1`$ and $`\mathbf{u}_2`$. The projection of $`\mathbf{v}`$ onto the plane is:

$$
\text{proj}_{\text{Plane}}(\mathbf{v}) = \frac{\mathbf{v} \cdot \mathbf{u}_1}{\|\mathbf{u}_1\|^2} \mathbf{u}_1 + \frac{\mathbf{v} \cdot \mathbf{u}_2}{\|\mathbf{u}_2\|^2} \mathbf{u}_2
$$

---

## **3. Calculating the Distance Between a Vector and a Subspace Spanned by Orthogonal Vectors**

The **distance** from a vector $`\mathbf{v}`$ to a subspace $W$ is the norm of the **orthogonal component**:

$$
\text{distance} = \|\mathbf{v} - \text{proj}_W(\mathbf{v})\|
$$

This gives the shortest distance between $`\mathbf{v}`$ and any vector in $W$.

---

## **4. Calculating the Acute Angle Between a Vector and a Subspace Spanned by Orthogonal Vectors**

Let $\theta$ be the **angle** between $`\mathbf{v}`$ and the subspace $W$. Then:

$$
\cos(\theta) = \frac{\|\text{proj}_W(\mathbf{v})\|}{\|\mathbf{v}\|}
\Rightarrow
\theta = \cos^{-1} \left( \frac{\|\text{proj}_W(\mathbf{v})\|}{\|\mathbf{v}\|} \right)
$$

This measures the closest angle between $`\mathbf{v}`$ and any vector in the subspace.

---

## **Summary Table**

| Concept                                             | Formula                                                                         |
| --------------------------------------------------- | ------------------------------------------------------------------------------- |
| Projection onto orthogonal basis $`\{\mathbf{u}_i\}`$ | $`\sum \frac{\mathbf{v} \cdot \mathbf{u}_i}{\|\mathbf{u}_i\|^2} \mathbf{u}_i`$    |
| Distance to subspace $W$                            | $`\|\mathbf{v} - \text{proj}_W(\mathbf{v})\|`$                                    |
| Angle to subspace $W$                               | $`\cos^{-1} \left( \frac{\|\text{proj}_W(\mathbf{v})\|}{\|\mathbf{v}\|} \right)`$ |

---

Orthogonal projections form the foundation for techniques like **least squares**, **Fourier approximations**, and **dimensionality reduction**. 
The orthogonality condition allows efficient and unique decomposition of vectors into subspace-aligned and orthogonal components.
