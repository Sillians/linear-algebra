## **Invertible Matrix Theorem — (Dimension, Rank, and Nullity)**

---

### **1. Overview: The Invertible Matrix Theorem (IMT)**

The Invertible Matrix Theorem (IMT) provides a list of logically equivalent statements about a square matrix $A \in \mathbb{R}^{n \times n}$. If **any one** of these statements is **true**, they **all are** — and if any is **false**, they **all are**.

---

### **2. Core Linear Algebra Concepts**

| Concept                                      | Definition                                                                   |
| -------------------------------------------- | ---------------------------------------------------------------------------- |
| **Rank**                                     | Dimension of the column space of $A$, denoted $\text{rank}(A)$               |
| **Nullity**                                  | Dimension of the null space of $A$, denoted $\text{nullity}(A)$              |
| **Dimension Theorem** (Rank-Nullity Theorem) | $\text{rank}(A) + \text{nullity}(A) = n$ for $A \in \mathbb{R}^{n \times n}$ |

---

### **3. Statements of the Invertible Matrix Theorem**

Let $A \in \mathbb{R}^{n \times n}$. The following are equivalent:

| #  | Statement                                                                            |
| -- | ------------------------------------------------------------------------------------ |
| 1  | $A$ is invertible                                                                    |
| 2  | $\det(A) \neq 0$                                                                     |
| 3  | The rank of $A$ is $n$: $\text{rank}(A) = n$                                         |
| 4  | $\text{nullity}(A) = 0$                                                              |
| 5  | $A \vec{x} = \vec{b}$ has a **unique solution** for every $\vec{b} \in \mathbb{R}^n$ |
| 6  | $A \vec{x} = \vec{0}$ has only the **trivial solution**                              |
| 7  | Columns of $A$ are **linearly independent**                                          |
| 8  | Columns of $A$ **span** $\mathbb{R}^n$                                               |
| 9  | The transformation $T(\vec{x}) = A\vec{x}$ is **one-to-one** and **onto**            |
| 10 | $A$ is row-equivalent to the identity matrix $I_n$                                   |
| 11 | The reduced row echelon form (RREF) of $A$ is $I_n$                                  |
| 12 | The matrix $A^T$ is invertible                                                       |

---

### **4. Recognizing Parts of the IMT**

To identify which property is being tested, associate keywords:

| Clue                                     | Related Statement |
| ---------------------------------------- | ----------------- |
| "unique solution"                        | #5                |
| "trivial solution to homogeneous system" | #6                |
| "linearly independent columns"           | #7                |
| "columns span $\mathbb{R}^n$"            | #8                |
| "onto" or "one-to-one"                   | #9                |
| "RREF is identity"                       | #11               |
| "rank = n"                               | #3                |
| "nullity = 0"                            | #4                |

---

### **5. Identifying True Statements Using the IMT**

Given a matrix $A \in \mathbb{R}^{n \times n}$, if **any one** of the following is true:

* $\text{rank}(A) = n$
* $\det(A) \neq 0$
* $A\vec{x} = \vec{b}$ has a unique solution
* $A$ is invertible

Then all other IMT statements are **true**.

**Examples:**

* If $\text{nullity}(A) = 0$, then $A$ is invertible.
* If $A \vec{x} = 0$ has nontrivial solutions ⇒ $A$ is **not** invertible.

---

### **6. Completing a Sentence Using IMT**

**Examples:**

* If a square matrix $A$ has **linearly independent** columns, then...

  > ...its rank is $n$, nullity is 0, and it is invertible.

* If the **null space** of $A$ contains a **nonzero vector**, then...

  > ...$A$ is not invertible, rank $< n$, and the columns are linearly dependent.

* If the **reduced row echelon form** of $A$ is the identity, then...

  > ...$A$ is invertible, and $\text{rank}(A) = n$, $\text{nullity}(A) = 0$.

---

### **7. Summary Table: IMT in Terms of Dimension, Rank, and Nullity**

| Property                                    | Invertible Matrix (Yes/No) | Rank of $A$ | Nullity of $A$ |
| ------------------------------------------- | -------------------------- | ----------- | -------------- |
| Full rank $\Rightarrow \text{rank}(A) = n$  | ✅ Yes                      | $n$         | 0              |
| Not full rank                               | ❌ No                       | $< n$       | $> 0$          |
| Linearly dependent columns                  | ❌ No                       | $< n$       | $> 0$          |
| Unique solution to all $A\vec{x} = \vec{b}$ | ✅ Yes                      | $n$         | 0              |
| Only trivial solution to $A\vec{x} = 0$     | ✅ Yes                      | $n$         | 0              |

---

### **8. Practice Questions**

**Q1:** If $\text{nullity}(A) = 0$, what is true?

* $A$ is invertible
* Columns of $A$ are linearly independent
* $\text{rank}(A) = n$

✅ All are true (from IMT).

**Q2:** If $A \vec{x} = 0$ has a nontrivial solution...

* Then $A$ is not invertible
* Columns of $A$ are not linearly independent
* $\text{nullity}(A) > 0$

✅ All are true.

---

Let me know if you'd like this as a printable summary or interactive quiz format.
