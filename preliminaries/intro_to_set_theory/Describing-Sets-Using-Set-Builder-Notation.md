## **Describing Sets Using Set-Builder Notation**

**Set-builder notation** allows us to define a set by specifying a **property** or **rule** that its elements must satisfy. 
Rather than listing elements explicitly, we use mathematical conditions to describe them, which is especially useful for infinite or patterned sets.

---

### **1. What Is Set-Builder Notation?**

A general form:

$$
\{ x \in S : \text{condition on } x \}
$$

* $`x`$ is a typical element.


* $`S`$ is the universal or relevant set (e.g., $`\mathbb{N}`$, $`\mathbb{Z}`$, $`\mathbb{R}`$).


* The condition specifies which $`x`$ belong.

---

###  **2. Expressing a Given Set Using an Arithmetic Sequence**

If a set follows a fixed pattern of **addition**, it’s an arithmetic sequence.

#### ✅ Example:

$$
\{ 3, 7, 11, 15, \ldots \}
$$

* First term: 3
* Common difference: 4

**Set-builder form**:

$$
\{ x \in \mathbb{N} : x = 4n - 1,\ n \in \mathbb{N} \}
$$

---

###  **3. Expressing a Given Set Using a Geometric Sequence**

If a set follows a pattern of **multiplication**, it’s a geometric sequence.

#### ✅ Example:

$$
\{ 2, 4, 8, 16, \ldots \}
$$

* First term: 2
* Ratio: 2

**Set-builder form**:

$$
\{ x \in \mathbb{N} : x = 2^n,\ n \in \mathbb{N}_0 \}
$$

---

###  **4. Expressing a Set Using a Conditional Definition**

You can define a set by imposing a logical or algebraic condition.

#### ✅ Example:

Set of even integers:

$$
\{ x \in \mathbb{Z} : x \equiv 0 \mod 2 \}
\quad \text{or} \quad
\{ x \in \mathbb{Z} : x = 2n,\ n \in \mathbb{Z} \}
$$

Set of all real numbers greater than 1:

$$
\{ x \in \mathbb{R} : x > 1 \}
$$

---

###  **5. Defining a Set Conditionally Using the Roots of a Polynomial**

You can define a set by identifying all values of $x$ that satisfy a polynomial equation.

#### ✅ Example:

$$
\text{Let } f(x) = x^2 - 5x + 6
$$

Find the set of real roots:

* Solve $`f(x) = 0 \Rightarrow x = 2 \text{ or } 3`$

**Set-builder form**:

$$
\{ x \in \mathbb{R} : x^2 - 5x + 6 = 0 \}
= \{ 2, 3 \}
$$

---

### ✅ **Summary Table**

| Set Type               | Set-Builder Notation Example          |
| ---------------------- | ------------------------------------- |
| Arithmetic Sequence    | $`\{ x \in \mathbb{N} : x = a + nd \}`$ |
| Geometric Sequence     | $`\{ x \in \mathbb{R} : x = ar^n \}`$   |
| Conditional Definition | $`\{ x \in \mathbb{R} : x > 1 \}`$      |
| Roots of a Polynomial  | $`\{ x \in \mathbb{R} : f(x) = 0 \}`$   |

---

### **Conclusion**

Set-builder notation is a concise and powerful tool for expressing structured or infinite sets. 
Whether defining numeric sequences, imposing conditions, or solving equations, it allows for precise mathematical communication of set membership.
