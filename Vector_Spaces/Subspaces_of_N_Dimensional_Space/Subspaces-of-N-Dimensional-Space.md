## **Subspaces of N-Dimensional Space, Deep Dive**

A **subspace** of $`\mathbb{R}^n`$ is a subset that is also a vector space under the same operations of vector addition and scalar multiplication.

To be a subspace, a set $`S \subseteq \mathbb{R}^n`$ must satisfy:

1. **Zero Vector**: $`\mathbf{0} \in S`$
2. **Closure under Addition**: If $`\mathbf{u}, \mathbf{v} \in S`$, then $`\mathbf{u} + \mathbf{v} \in S`$
3. **Closure under Scalar Multiplication**: If $`\mathbf{v} \in S`$ and $`c \in \mathbb{R}`$, then $`c\mathbf{v} \in S`$

---

## **Examples of Subspaces**

* The zero subspace: $`\{ \mathbf{0} \}`$


* Any line through the origin in $`\mathbb{R}^2`$ or $`\mathbb{R}^3`$


* Any plane through the origin in $`\mathbb{R}^3`$


* The entire space $`\mathbb{R}^n`$

---

## **Determining Whether a Line Is a Subspace of $`\mathbb{R}^2`$**

A line in $`\mathbb{R}^2`$ is a subspace **if and only if** it passes through the origin and is closed under vector operations.

**Example 1** (Subspace):

A line defined by:

$$
y = 2x
$$

Can be written as:

$$
\{ (x, 2x) \mid x \in \mathbb{R} \} = \{ x(1, 2) \mid x \in \mathbb{R} \}
$$

This is a subspace of $`\mathbb{R}^2`$.

**Example 2** (Not a Subspace):

A line defined by:

$$
y = 2x + 1
$$

Fails the zero vector test: $`(0, 1) \notin \mathbb{R}^2`$ → **Not a subspace**.

---

## **Determining Whether a Line Is a Subspace of $`\mathbb{R}^3`$**

A line in $`\mathbb{R}^3`$ is a subspace **if** it can be written as:
``
$$
\{ t\mathbf{v} \mid t \in \mathbb{R} \}
$$

Where $`\mathbf{v} \in \mathbb{R}^3`$.

**Example**:

$$
\{ t(1, 2, 3) \mid t \in \mathbb{R} \}
$$

Is a line through the origin → **Subspace**.

---

## **Determining Whether a Plane Is a Subspace of $`\mathbb{R}^3`$**

A plane in $`\mathbb{R}^3`$ is a subspace **if and only if** it passes through the origin and satisfies the closure properties.

**Example 1** (Subspace):

$$
\{ a(1, 0, 0) + b(0, 1, 0) \mid a, b \in \mathbb{R} \}
$$

This is the $xy$-plane → **Subspace**.

**Example 2** (Not a Subspace):

$$
x + y + z = 1
$$

This plane does **not** contain the zero vector:

$$
x = y = z = 0 \Rightarrow 0 + 0 + 0 = 0 \neq 1
$$

→ **Not a subspace**

---

## **Summary: Conditions for a Subspace**

A set $`S \subseteq \mathbb{R}^n`$ is a subspace if:

* $`\mathbf{0} \in S`$


* $`\forall \mathbf{u}, \mathbf{v} \in S,\ \mathbf{u} + \mathbf{v} \in S`$


* $`\forall \mathbf{v} \in S,\ \forall c \in \mathbb{R},\ c\mathbf{v} \in S`$

A line or plane **must** pass through the origin to be a subspace.
