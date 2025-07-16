## **Change of Variables in Quadratic Forms**

---

## Overview

A **quadratic form** in vector notation is typically written as:

$$
Q(\vec{x}) = \vec{x}^T A \vec{x}
$$

Where:

* $`\vec{x}`$ is a vector of variables
* $A$ is a symmetric matrix

When changing variables via a **change-of-coordinates matrix** $P$, such that:

$$
\vec{x} = P\vec{y}
$$

The quadratic form becomes:

$$
Q(\vec{x}) = (P\vec{y})^T A (P\vec{y}) = \vec{y}^T (P^T A P) \vec{y}
$$

Thus, $`B = P^T A P`$ is the matrix of the quadratic form in the new coordinates.

---

## 1. Changing Variables in a Quadratic Form Given Old Variables Through New Variables

Given the relationship $`\vec{x} = P\vec{y}`$:

* Substitute into the quadratic form $`Q(\vec{x}) = \vec{x}^T A \vec{x}`$
* You get:

$$
Q(\vec{x}) = \vec{y}^T (P^T A P) \vec{y}
$$

* The transformed matrix of the quadratic form in new variables is $`B = P^T A P`$

**Example**
Let:

* $`A = \begin{pmatrix} 2 & 1 \ 1 & 3 \end{pmatrix}`$
* $`P = \begin{pmatrix} 1 & 1 \ 0 & 1 \end{pmatrix}`$

Then:

$$
B = P^T A P = \begin{pmatrix} 1 & 0 \\ 1 & 1 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 1 & 3 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}
= \begin{pmatrix} 2 & 3 \\ 3 & 6 \end{pmatrix}
$$

---

## 2. Changing Variables in a Quadratic Form Given New Variables Through Old Variables

If the relationship is given as:

$$
\vec{y} = P^{-1} \vec{x}
$$

Then $`\vec{x} = P \vec{y}`$, and the process is the same as above.

* Substitute $`\vec{x} = P \vec{y}`$ into $`Q(\vec{x})`$
* Get the new form:

$$
Q(\vec{y}) = \vec{y}^T (P^T A P) \vec{y}
$$

So the process still uses the transformation matrix $P$, not $`P^{-1}`$, in the similarity transform.

---

## 3. Finding the Matrix of a Quadratic Form Given a Change-of-Coordinates Matrix

Given:

* Original matrix $A$ of the quadratic form in the standard basis
* Change-of-coordinates matrix $P$ (from new basis to standard basis)

To find the new matrix $B$ in the new coordinate system:

$$
B = P^T A P
$$

This matrix represents the same quadratic form under the new variable system.

**Use Cases**:

* Diagonalizing quadratic forms
* Simplifying conic sections or energy functions in physics
* Changing orthogonal bases in vector spaces

---

## 📌 Summary Table

| Task                                      | Formula / Method                                                      |
| ----------------------------------------- | --------------------------------------------------------------------- |
| Change of variables (old → new)           | $`\vec{x} = P\vec{y} \Rightarrow Q(\vec{x}) = \vec{y}^T (P^T A P) \vec{y}`$ |
| Change of variables (new → old)           | $`\vec{y} = P^{-1} \vec{x} \Rightarrow`$ same form as above using $P$  |
| Matrix of quadratic form in new variables | $`B = P^T A P`$                                                        |

---


