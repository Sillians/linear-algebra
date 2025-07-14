# **Inner Product Spaces**

An **inner product space** is a vector space equipped with an inner product — a generalization of the dot product 
that enables measurement of angles, lengths, and orthogonality.

---

## **Definition of an Inner Product**

An **inner product** on a vector space $V$ over $`\mathbb{R}`$ or $`\mathbb{C}`$ is a function:

$$
\langle \cdot, \cdot \rangle : V \times V \to \mathbb{R} \ \text{or} \ \mathbb{C}
$$

such that for all $`\mathbf{u}, \mathbf{v}, \mathbf{w} \in V`$ and scalar $`\alpha`$:

1. **Conjugate symmetry**: $`\langle \mathbf{u}, \mathbf{v} \rangle = \overline{\langle \mathbf{v}, \mathbf{u} \rangle}`$


2. **Linearity in the first argument**: $`\langle \alpha \mathbf{u} + \mathbf{v}, \mathbf{w} \rangle = \alpha \langle \mathbf{u}, \mathbf{w} \rangle + \langle \mathbf{v}, \mathbf{w} \rangle`$


4. **Positive-definiteness**: $`\langle \mathbf{v}, \mathbf{v} \rangle \ge 0`$, with equality only if $`\mathbf{v} = \mathbf{0}`$

---

##  **Calculating the Inner Product of Two Vectors (Euclidean Space)**

In $`\mathbb{R}^n`$, the standard inner product (dot product) is:

$$
\langle \mathbf{u}, \mathbf{v} \rangle = \sum_{i=1}^n u_i v_i
$$

**Example:**

Let $`\mathbf{u} = [1, 2, 3]`$, $`\mathbf{v} = [4, 0, -1]`$
Then:

$$
\langle \mathbf{u}, \mathbf{v} \rangle = 1(4) + 2(0) + 3(-1) = 4 + 0 - 3 = 1
$$

---

##  **Inner Product in a Vector Space of Polynomials**

For the vector space $`P\_2`$ (polynomials of degree ≤ 2), define:

$$
\langle p, q \rangle = \int_{-1}^{1} p(x) q(x) \, dx
$$

**Example:**

Let $`p(x) = 1 + x`$, $`q(x) = x`$
Then:

$$
\langle p, q \rangle = \int_{-1}^{1} (1 + x)(x) \, dx
= \int_{-1}^{1} (x + x^2) \, dx
= \left[ \frac{x^2}{2} + \frac{x^3}{3} \right]_{-1}^1
= \left( \frac{1}{2} + \frac{1}{3} \right) - \left( \frac{1}{2} - \frac{1}{3} \right) = \frac{2}{3}
$$

---

##  **Inner Product in a Space of Continuous Functions**

In $`C[a, b]`$, the space of continuous real-valued functions on $`[a, b]`$, define:

$$
\langle f, g \rangle = \int_a^b f(x) g(x) \, dx
$$

**Example:**

Let $`f(x) = \sin x`$, $`g(x) = \cos x`$ on $`[0, \pi]`$

Then:

$$
\langle f, g \rangle = \int_0^{\pi} \sin x \cos x \, dx
= \frac{1}{2} \int_0^{\pi} \sin(2x) \, dx
= \left[ -\frac{1}{4} \cos(2x) \right]_0^{\pi} = 0
$$

$`\Rightarrow`$ $`\sin x`$ and $`\cos x`$ are **orthogonal** on $`[0, \pi]`$

---

##  **Summary Table**

| Vector Space          | Inner Product                                               |
| --------------------- |-------------------------------------------------------------|
| $`\mathbb{R}^n`$      | $`\langle \mathbf{u}, \mathbf{v} \rangle = \sum u\_i v\_i`$ |
| $`P\_n`$ (Polynomials) | $`\langle p, q \rangle = \int\_a^b p(x) q(x) , dx`$         |
| $`C[a,b]`$ (Functions) | $`\langle f, g \rangle = \int\_a^b f(x) g(x) , dx`$         |

---
