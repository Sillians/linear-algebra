## **Orthogonal Sets in Euclidean Spaces**

---

### **1. Overview of Orthogonal Sets**

An **orthogonal set** in a Euclidean space is a set of vectors in which every pair of distinct vectors is 
orthogonal—that is, their dot product is zero. If, in addition, each vector is a **unit vector** (has length 1), 
the set is called **orthonormal**.

#### Definitions:

* **Orthogonal set**: A set of vectors $`\{ \mathbf{v}_1, \mathbf{v}_2, ..., \mathbf{v}_n \}`$ such that $`\mathbf{v}_i \cdot \mathbf{v}_j = 0`$ for all $`i \ne j`$.
* **Orthonormal set**: An orthogonal set in which $`\|\mathbf{v}_i\| = 1`$ for all $i$.

---

### **2. Determining Whether Sets Are Orthogonal**

To check if a set is **orthogonal**, compute the pairwise dot products:

For $`\{\mathbf{u}, \mathbf{v}, \mathbf{w}\} \subset \mathbb{R}^n`$, check:

* $`\mathbf{u} \cdot \mathbf{v} = 0`$


* $`\mathbf{u} \cdot \mathbf{w} = 0`$


* $`\mathbf{v} \cdot \mathbf{w} = 0`$

If all are zero, the set is orthogonal.

> **Note:** Zero vector **cannot** be part of an orthogonal set since it's orthogonal to everything but has zero norm.

---

### **3. Determining Whether Sets Are Orthonormal**

To check if a set is **orthonormal**, perform two checks:

* All vectors are orthogonal (as above).


* Each vector has norm 1: $`\|\mathbf{v}_i\| = \sqrt{\mathbf{v}_i \cdot \mathbf{v}_i} = 1`$


If both conditions are satisfied, the set is orthonormal.

---

### **4. Extending a Set to Form an Orthogonal Basis**

To extend a set $`\{\mathbf{v}_1, ..., \mathbf{v}_k\} \subset \mathbb{R}^n`$ to an **orthogonal basis** of $`\mathbb{R}^n`$:

* Use the **Gram-Schmidt process**.


* Add new linearly independent vectors and orthogonalize them against the existing set.


**Example:**

Start with $`\mathbf{v}_1`$. Add $`\mathbf{v}_2`$, and orthogonalize:

$$
\mathbf{u}_2 = \mathbf{v}_2 - \frac{\mathbf{v}_2 \cdot \mathbf{u}_1}{\|\mathbf{u}_1\|^2} \mathbf{u}_1
$$

Continue until you have $n$ linearly independent vectors.

---

### **5. Extending a Set to Form an Orthonormal Basis**

Once you have an **orthogonal set**, convert it to an **orthonormal basis** by **normalizing** each vector:

$$
\mathbf{w}_i = \frac{\mathbf{u}_i}{\|\mathbf{u}_i\|}
$$

If you're starting from linearly independent vectors:

* Apply **Gram-Schmidt** to make them orthogonal.
* Normalize each resulting vector to obtain orthonormality.

---

### **Summary Table**

| Property              | Orthogonal Set                                      | Orthonormal Set                      |
| --------------------- | --------------------------------------------------- | ------------------------------------ |
| Dot product condition | $`\mathbf{v}_i \cdot \mathbf{v}_j = 0`$ for $`i \ne j`$ | Same as orthogonal                   |
| Norm condition        | Vectors may have arbitrary length                   | $`\|\mathbf{v}_i\| = 1`$ for all $i$   |
| Zero vector allowed?  | No                                                  | No                                   |
| Used in               | Constructing bases, simplifying projections         | Orthogonal matrices, Fourier methods |

---

### **Key Applications**

* Simplifying vector projections
* Constructing orthogonal or orthonormal bases for subspaces
* Basis change in vector spaces
* Spectral theorems and diagonalization (orthonormal eigenvectors)
