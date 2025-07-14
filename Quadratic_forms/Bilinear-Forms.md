## **Bilinear Forms**

---

## **1. Bilinear Forms: Definition**

A **bilinear form** on a vector space $V$ over a field $`\mathbb{F}`$ is a function:

$$
B : V \times V \to \mathbb{F}
$$

such that it is **linear in each argument**, i.e., for all $`u, v, w \in V`$ and $`\alpha \in \mathbb{F}`$:

* $`B(u + v, w) = B(u, w) + B(v, w)`$, and $`B(\alpha u, w) = \alpha B(u, w)`$
* $`B(u, v + w) = B(u, v) + B(u, w)`$, and $`B(u, \alpha v) = \alpha B(u, v)`$

---

## **2. Evaluating a Linear Form**

A **linear form** (or linear functional) is a map:

$$
\ell: V \to \mathbb{F}
$$

that satisfies:

$$
\ell(a v + b w) = a \ell(v) + b \ell(w)
$$

If $`v \in \mathbb{F}^n`$ and $`c \in \mathbb{F}^n`$, then:

$$
\ell(v) = c^T v = \sum_{i=1}^n c_i v_i
$$

**Example**:

Let $`c = [2, -1, 3]`$, $`v = [1, 4, 2]`$:

$$
\ell(v) = 2(1) + (-1)(4) + 3(2) = 2 - 4 + 6 = 4
$$

---

## **3. Evaluating a Bilinear Form**

Given a bilinear form represented by a matrix $`A \in \mathbb{F}^{n \times n}`$, for $`u, v \in \mathbb{F}^n`$:

$$
B(u, v) = u^T A v
$$

**Example**:

Let

$$
u = \begin{bmatrix}1 \\ 2\end{bmatrix}, \quad v = \begin{bmatrix}3 \\ 4\end{bmatrix}, \quad A = \begin{bmatrix}1 & 2 \\ 0 & 3\end{bmatrix}
$$

Then

$$
B(u, v) = [1\ 2] \begin{bmatrix}1 & 2 \\ 0 & 3\end{bmatrix} \begin{bmatrix}3 \\ 4\end{bmatrix} = [1, 8] \cdot \begin{bmatrix}3 \\ 4\end{bmatrix} = 3 + 32 = 35
$$

---

## **4. Writing Down a Bilinear Form Given Its Matrix**

Given $`A \in \mathbb{F}^{n \times n}`$, the bilinear form can be written as:

$$
B(x, y) = x^T A y = \sum_{i=1}^n \sum_{j=1}^n A_{ij} x_i y_j
$$

**Example**:

Let

$$
A = \begin{bmatrix}2 & 1 \\ 1 & 3\end{bmatrix}
$$

Then

$$
B(x, y) = 2x_1y_1 + x_1y_2 + x_2y_1 + 3x_2y_2
$$

---

## **5. Finding the Matrix of a Bilinear Form**

Given the symbolic expression of a bilinear form:

$$
B(x, y) = 2x_1y_1 + x_1y_2 + x_2y_1 + 3x_2y_2
$$

Match coefficients with:

$$
B(x, y) = \sum_{i=1}^n \sum_{j=1}^n A_{ij} x_i y_j
$$

Identify matrix entries:

* $`A_{11} = 2`$
* $`A_{12} = 1`$
* $`A_{21} = 1`$
* $`A_{22} = 3`$

So,

$$
A = \begin{bmatrix}2 & 1 \\ 1 & 3\end{bmatrix}
$$

---

## **Summary Table**

| **Task**                        | **Formula / Method**                             |
| ------------------------------- | ------------------------------------------------ |
| Linear Form                     | $`\ell(v) = c^T v`$                                |
| Evaluate Bilinear Form          | $`B(u, v) = u^T A v`$                              |
| Write Bilinear Form from Matrix | Expand $`B(x, y) = x^T A y = \sum A_{ij} x_i y_j`$ |
| Find Matrix from Symbolic Form  | Match terms with $`A_{ij} x_i y_j`$                |


