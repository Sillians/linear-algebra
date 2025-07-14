# **Defining Abstract Vector Spaces**

---

## **1. What Is an Abstract Vector Space?**

An **abstract vector space** (or linear space) is a set $`V`$ equipped with:

* A **vector addition** operation: $`+ : V \times V \to V`$
* A **scalar multiplication** operation: $`\cdot : \mathbb{F} \times V \to V`$

Where $`\mathbb{F}`$ is a **field** (e.g., $`\mathbb{R}`$ or $`\mathbb{C}`$), and the operations satisfy **eight axioms** (closure, associativity, identity, inverses, distributivity, etc.).

---

## **2. Formal Definition of a Vector Space**

Let $V$ be a non-empty set over a field $`\mathbb{F}`$ (typically $`\mathbb{R}`$). Then $`V`$ is a **vector space** 
if for all $`\mathbf{u}, \mathbf{v}, \mathbf{w} \in V`$ and all scalars $`a, b \in \mathbb{F}`$:

---

### **Vector Space Axioms**

1. **Additive Closure**:
   $`\mathbf{u} + \mathbf{v} \in V`$

2. **Commutativity of Addition**:
   $`\mathbf{u} + \mathbf{v} = \mathbf{v} + \mathbf{u}`$

3. **Associativity of Addition**:
   $`(\mathbf{u} + \mathbf{v}) + \mathbf{w} = \mathbf{u} + (\mathbf{v} + \mathbf{w})`$

4. **Additive Identity**:
   There exists a zero vector $`\mathbf{0} \in V`$ such that:
   $`\mathbf{v} + \mathbf{0} = \mathbf{v}`$

5. **Additive Inverses**:
   For each $`\mathbf{v} \in V`$, there exists $`- \mathbf{v} \in V`$ such that:
   $`\mathbf{v} + (-\mathbf{v}) = \mathbf{0}`$

6. **Scalar Multiplication Closure**:
   $`a \cdot \mathbf{v} \in V`$

7. **Distributivity Over Vector Addition**:
   $`a \cdot (\mathbf{u} + \mathbf{v}) = a \cdot \mathbf{u} + a \cdot \mathbf{v}`$

8. **Distributivity Over Scalar Addition**:
   $`(a + b) \cdot \mathbf{v} = a \cdot \mathbf{v} + b \cdot \mathbf{v}`$

9. **Associativity of Scalar Multiplication**:
   $`a \cdot (b \cdot \mathbf{v}) = (ab) \cdot \mathbf{v}`$

10. **Scalar Identity**:
    $`1 \cdot \mathbf{v} = \mathbf{v}`$

---

## **3. Examples of Vector Spaces**

| Set                            | Description                          |
| ------------------------------ | ------------------------------------ |
| $`\mathbb{R}^n`$                 | Euclidean vectors                    |
| Space of polynomials           | Functions of the form $`p(x)`$         |
| Matrix spaces $`M_{m \times n}`$ | All $`m \times n`$ real matrices       |
| $`C([a, b])`$                    | Continuous functions on $`[a,b]`$      |
| $`\mathbb{R}^\infty`$            | Infinite sequences (with conditions) |

---

## **4. Identifying Sets That Are Not Vector Spaces**

To disprove that a set is a vector space, **show that one of the axioms fails**.

### **Example 1:**

Let $`V = \{ \mathbf{x} \in \mathbb{R}^2 \mid x_1 \geq 0 \}`$

* Not closed under scalar multiplication. For $`\mathbf{x} = [1, 2]^T`$ and scalar $`-1`$:

$$
-1 \cdot \mathbf{x} = [-1, -2]^T \notin V
$$

### **Example 2:**

Let $`V = \{ \mathbf{x} \in \mathbb{R}^2 \mid x_1 + x_2 = 1 \}`$

* Not closed under addition:
  $`[1, 0]^T + [0, 1]^T = [1, 1]^T`$, but $`1 + 1 \ne 1`$

---

## **5. Proving Statements Using the Vector Space Axioms**

### **Example Proof: Zero Vector Uniqueness**

**Claim**: The zero vector in a vector space is unique.

**Proof**:

Assume $`\mathbf{0}`$ and $`\mathbf{0}'`$ both satisfy:

$$
\mathbf{v} + \mathbf{0} = \mathbf{v}, \quad \mathbf{v} + \mathbf{0}' = \mathbf{v}
$$

Then:

$$
\mathbf{0} = \mathbf{0} + \mathbf{0}' = \mathbf{0}'
$$

⇒ The zero vector is unique. □

---

### **Example Proof: Negative Vector Uniqueness**

**Claim**: The additive inverse of a vector is unique.

Let $`\mathbf{v} + \mathbf{u} = \mathbf{0}`$ and $`\mathbf{v} + \mathbf{w} = \mathbf{0}`$

Then:

$$
\mathbf{u} = \mathbf{u} + \mathbf{0} = \mathbf{u} + (\mathbf{v} + \mathbf{w}) = (\mathbf{u} + \mathbf{v}) + \mathbf{w} = \mathbf{0} + \mathbf{w} = \mathbf{w}
$$

⇒ The additive inverse is unique. □

---

## ✅ Summary Table

| Concept                         | Description                                                             |
| ------------------------------- | ----------------------------------------------------------------------- |
| Vector space                    | Set with vector addition and scalar multiplication satisfying 10 axioms |
| Not a vector space              | Fails at least one axiom (e.g., closure, identity, inverse)             |
| Proving vector space properties | Use axioms to derive uniqueness or other properties                     |

---
