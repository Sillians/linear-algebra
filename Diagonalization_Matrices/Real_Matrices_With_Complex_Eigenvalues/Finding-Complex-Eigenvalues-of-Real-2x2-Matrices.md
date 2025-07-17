## **Finding Complex Eigenvalues of Real 2×2 Matrices**

Eigenvalues of a real $`2 \times 2`$ matrix can be real or complex. Complex eigenvalues often appear in conjugate pairs when the characteristic polynomial has no real roots.

---

### **1. Computing the Complex Eigenvalues of a Matrix**

Let

$`A = \begin{bmatrix} a & b \\ c & d \end{bmatrix}`$

The **characteristic polynomial** is obtained by solving:

$`\det(A - \lambda I) = 0 \Rightarrow \begin{vmatrix} a - \lambda & b \\c & d - \lambda \end{vmatrix} = 0`$


$`\Rightarrow \lambda^2 - (a + d)\lambda + (ad - bc) = 0`$


This is a quadratic equation:

$`\lambda^2 - \mathrm{tr}(A)\lambda + \det(A) = 0`$

Let:

* $`\mathrm{tr}(A) = a + d`$ (the trace),


* $`\det(A) = ad - bc`$
* 

Use the quadratic formula:

$`\lambda = \frac{\mathrm{tr}(A) \pm \sqrt{\mathrm{tr}(A)^2 - 4\det(A)}}{2}`$


If the discriminant is **negative**, the eigenvalues are complex conjugates.

---

**Example**
Let

$`A = \begin{bmatrix} 0 & -1 \\ 1 & 0 \end{bmatrix}`$

Then:

* $`\mathrm{tr}(A) = 0`$


* $`\det(A) = (0)(0) - (-1)(1) = 1`$


$`\lambda = \frac{0 \pm \sqrt{0^2 - 4(1)}}{2} = \pm \frac{\sqrt{-4}}{2} = \pm i`$

So, the eigenvalues are $i$ and $-i$.

---

### **2. Finding a Complex Eigenvalue Given Another**

If one complex eigenvalue of a real matrix is known (say $`\lambda = a + bi`$, $`b \ne 0`$), then the **other eigenvalue** must be its complex conjugate:


$`\bar{\lambda} = a - bi`$


This is guaranteed by the **Complex Conjugate Root Theorem**, applicable to real-coefficient polynomials.

---

**Example**
Given a real matrix has one eigenvalue $`3 + 4i`$, the second must be:

$`\bar{\lambda} = 3 - 4i`$

---

### Summary Table

| Concept                      | Description                                         |
| ---------------------------- |-----------------------------------------------------|
| Characteristic Polynomial    | $`\lambda^2 - \mathrm{tr}(A)\lambda + \det(A) = 0`$ |
| Complex Eigenvalues          | Occur when discriminant $`< 0`$                     |
| Eigenvalues of Real Matrix   | Always occur in conjugate pairs if complex          |
| Given One Complex Eigenvalue | The other is its complex conjugate                  |

---
