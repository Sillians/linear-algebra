## **The Rank-Nullity Theorem in Terms of Linear Transformations**

---

### **I. Overview: Rank-Nullity Theorem**

Let $`T: V \rightarrow W`$ be a **linear transformation** between finite-dimensional vector spaces.

The **Rank-Nullity Theorem** states:

$`\mathrm{dim}(V) = \mathrm{rank}(T) + \mathrm{nullity}(T)`$

where:

* $`\mathrm{dim}(V)`$: dimension of the domain.


* $`\mathrm{rank}(T) = \dim(\mathrm{Im}(T))`$: dimension of the image of $T$.


* $`\mathrm{nullity}(T) = \dim(\ker(T))`$: dimension of the kernel of $T$.

This relates the **structure of a linear transformation** to the **dimensions of its kernel and image**.

---

### **II. Matrix Formulation**

If $`T(x) = Ax`$, where $`A \in \mathbb{R}^{m \times n}`$, then:

$`\mathrm{rank}(A) + \mathrm{nullity}(A) = n`$

where:

* $`\mathrm{rank}(A) = \dim(\mathrm{col}(A))`$


* $`\mathrm{nullity}(A) = \dim(\ker(A))`$


* $`n =`$ number of columns of $A$

---

### **III. Finding the Rank or Nullity Using the Rank-Nullity Theorem**

#### **Example 1**:

Let $`T: \mathbb{R}^5 \rightarrow \mathbb{R}^3`$ be a linear transformation with $`\mathrm{nullity}(T) = 2`$. 
Find $`\mathrm{rank}(T)`$.

**Solution:**

$`\mathrm{dim}(\mathbb{R}^5) = \mathrm{rank}(T) + \mathrm{nullity}(T) \Rightarrow 5 = \mathrm{rank}(T) + 2 \Rightarrow \mathrm{rank}(T) = 3`$

#### **Example 2**:

Let $`A \in \mathbb{R}^{4 \times 6}`$ and $`\mathrm{rank}(A) = 4`$. Find $`\mathrm{nullity}(A)`$.

**Solution:**

$`\mathrm{nullity}(A) = 6 - \mathrm{rank}(A) = 6 - 4 = 2`$

---

### **IV. Finding Rank or Nullity Given a Description of the Image or Kernel**

#### **Example 3**:

Let $`T: \mathbb{R}^6 \rightarrow \mathbb{R}^4`$ and suppose:

* The image of $`T`$ is the span of 3 linearly independent vectors in $`\mathbb{R}^4`$.


* What is the nullity of $`T`$?


**Solution:**

* Rank = 3 (since image is 3D)


* Domain is $`\mathbb{R}^6`$, so:


$`\mathrm{nullity}(T) = 6 - 3 = 3`$


#### **Example 4**:

Let $`T: \mathbb{R}^5 \rightarrow \mathbb{R}^5`$ and suppose $`\ker(T) = \{0\}`$. What is $`\mathrm{rank}(T)`$?

**Solution:**

* Nullity = 0 ⇒ $`\mathrm{rank}(T) = 5`$

This means $T$ is **injective** (1–1).

---

### **V. Identifying True Statements Using the Rank-Nullity Theorem**

Given $`T: \mathbb{R}^n \to \mathbb{R}^m`$:


#### **Example 5**:

If $`\mathrm{nullity}(T) = 0`$, then:

* $`\ker(T) = \{0\}`$: True


* $`T`$ is injective (one-to-one): True


* $`\mathrm{rank}(T) = n`$: True


* If $`n > m`$, then $`T`$ is not surjective: True


#### **Example 6**:

If $`\mathrm{rank}(T) = m`$ and $`m < n`$, then:

* $`T`$ is surjective (onto): True
* $`T`$ is not injective: True (nullity $`> 0`$)

#### **Example 7**:

If $`\mathrm{rank}(T) = \mathrm{nullity}(T)`$, then $`\dim(V) = 2 \cdot \mathrm{rank}(T)`$

---

### **VI. Visual Summary**

| Symbol                  | Meaning                                              |
|-------------------------|------------------------------------------------------|
| $`\mathrm{rank}(T)`$    | Dimension of the image of $`T`$                      |
| $`\mathrm{nullity}(T)`$ | Dimension of the kernel of $`T`$                     |
| $`\dim(V)`$             | Dimension of the domain                              |
| $`T`$ is injective      | $`\ker(T) = \{0\} \Rightarrow \mathrm{nullity} = 0`$ |
| $`T`$ is surjective     | $`\mathrm{rank}(T) = \dim(W)`$                       |

---

### **VII. Conceptual Interpretations**

* The Rank-Nullity Theorem partitions the dimension of the domain into:


  * The part **mapped to zero** (nullity), and
  * The part **effectively used** in the codomain (rank)


* It is a **conservation law** of linear transformation dimensions.

---

This theorem is central in understanding:

* Injectivity and surjectivity of linear maps


* Solution spaces of linear systems


* Matrix rank and kernel dimension relationships
