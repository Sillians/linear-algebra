## **Ranks of Generalized Eigenvectors**

---

### **1. Overview: Generalized Eigenvectors and Their Ranks**

#### **Generalized Eigenvector Definition**

Let $`A \in \mathbb{C}^{n \times n}`$ and $`\lambda`$ be an eigenvalue of $A$. 
A nonzero vector $`\mathbf{v}`$ is a **generalized eigenvector** of **rank $`r`$** for $`\lambda`$ if:


$`(A - \lambda I)^r \mathbf{v} = 0 \quad \text{but} \quad (A - \lambda I)^{r-1} \mathbf{v} \neq 0.`$

* When $`r = 1`$, $`\mathbf{v}`$ is a regular eigenvector.


* When $`r > 1`$, $`\mathbf{v}`$ lies deeper in the **Jordan chain**.

---

### **2. Finding the Number of Generalized Eigenvectors of Rank Greater Than One**

To determine the number of generalized eigenvectors of rank $`> 1`$, we analyze the sequence of **nullities** of powers of $`(A - \lambda I)`$:

Let:

* $`N_k = \ker((A - \lambda I)^k)`$

Then:

* Generalized eigenvectors of **rank exactly $r$** lie in $`N_r \setminus N_{r-1}`$


* So, their **count** equals:

$`\dim(N_r) - \dim(N_{r-1})`$

#### **Total Number of Generalized Eigenvectors (all ranks)**

For eigenvalue $`\lambda`$ with algebraic multiplicity $m$,


$`\dim(\ker((A - \lambda I)^m)) = m`$

---

### **3. Finding the Number of Generalized Eigenvectors of a Given Rank Using Nullity**

Let $A$ be a $`3 \times 3`$ matrix with eigenvalue $`\lambda`$ of multiplicity 3. Define:

* $`N_1 = \ker(A - \lambda I)`$


* $`N_2 = \ker((A - \lambda I)^2)`$


* $`N_3 = \ker((A - \lambda I)^3)`$

Then:

* **Rank 1 generalized eigenvectors** = $`\dim(N_1)`$


* **Rank 2 generalized eigenvectors** = $`\dim(N_2) - \dim(N_1)`$


* **Rank 3 generalized eigenvectors** = $`\dim(N_3) - \dim(N_2)`$

#### **Example**

Let:

* $`\dim(N_1) = 1`$


* $`\dim(N_2) = 2`$


* $`\dim(N_3) = 3`$

Then:

* Rank 1: 1 eigenvector


* Rank 2: $`2 - 1 = 1`$


* Rank 3: $`3 - 2 = 1`$

So, total = 3 linearly independent generalized eigenvectors (matching algebraic multiplicity).

---

### **4. Finding the Number of Generalized Eigenvectors of a Given Rank**

For eigenvalue $`\lambda`$ and operator $`T = A - \lambda I`$, define the **chains of subspaces**:

$`\{0\} \subset \ker(T) \subset \ker(T^2) \subset \cdots \subset \ker(T^m)`$

The number of generalized eigenvectors of **rank $r$** is:

$`\dim(\ker(T^r)) - \dim(\ker(T^{r-1}))`$

This reflects how many **new directions** are added in the null space as we increase powers of $T$.

---

### **Summary Table**

| Rank $r$ | Condition                                           | Number of Generalized Eigenvectors        |
| -------- |-----------------------------------------------------|-------------------------------------------|
| 1        | $`T\mathbf{v} = 0`$                                 | $`\dim(\ker(T))`$                         |
| 2        | $`T^2\mathbf{v} = 0`$, $`T\mathbf{v} \neq 0`$       | $`\dim(\ker(T^2)) - \dim(\ker(T))`$       |
| 3        | $`T^3\mathbf{v} = 0`$, $`T^2\mathbf{v} \neq 0`$     | $`\dim(\ker(T^3)) - \dim(\ker(T^2))`$     |
| General  | $`T^r\mathbf{v} = 0`$, $`T^{r-1}\mathbf{v} \neq 0`$ | $`\dim(\ker(T^r)) - \dim(\ker(T^{r-1}))`$ |

---
