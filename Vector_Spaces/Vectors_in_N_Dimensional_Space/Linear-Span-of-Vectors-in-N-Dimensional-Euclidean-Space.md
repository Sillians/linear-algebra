## **Linear Span of Vectors in N-Dimensional Euclidean Space**

The **linear span** of a set of vectors is the collection of all **linear combinations** that can 
be formed from them. It's a foundational concept in linear algebra that helps define subspaces, 
solve systems of equations, and understand vector relationships.

---

### **1. Definition: Linear Span**

Let $`\mathbf{v}_1, \mathbf{v}_2, \dots, \mathbf{v}_k \in \mathbb{R}^n`$. The **span** of these vectors is:

$`\text{Span}\{\mathbf{v}_1, \dots, \mathbf{v}_k\} = \left\{ c_1\mathbf{v}_1 + c_2\mathbf{v}_2 + \dots + c_k\mathbf{v}_k \mid c_i \in \mathbb{R} \right\}`$

It’s the **smallest subspace** of $`\mathbb{R}^n`$ that contains all the vectors.

---

### **2. Determining Whether a Vector Lies in the Span of Given Vectors**

To determine whether a vector $`\mathbf{b}`$ lies in the span of $`\mathbf{v}_1, \mathbf{v}_2, \dots`$, check if there exist scalars $x_1, x_2, \dots$ such that:

$`x_1\mathbf{v}_1 + x_2\mathbf{v}_2 + \dots = \mathbf{b}`$

This forms a **system of linear equations**.

---

#### **Example:**

Let:

$$
\mathbf{v}_1 = \begin{bmatrix} 1 \\ 2 \end{bmatrix}, \quad
\mathbf{v}_2 = \begin{bmatrix} 3 \\ 1 \end{bmatrix}, \quad
\mathbf{b} = \begin{bmatrix} 6 \\ 5 \end{bmatrix}
$$


Check if $\mathbf{b} \in \text{Span}\{\mathbf{v}_1, \mathbf{v}_2\}$

Form:

$$
x_1\begin{bmatrix} 1 \\ 2 \end{bmatrix} + x_2\begin{bmatrix} 3 \\ 1 \end{bmatrix} = \begin{bmatrix} 6 \\ 5 \end{bmatrix}
\Rightarrow
\begin{cases}
x_1 + 3x_2 = 6 \\
2x_1 + x_2 = 5
\end{cases}
$$

Solving gives: $x_1 = 1, x_2 = \frac{5}{3}$ → **solution exists**, so $\mathbf{b}$ **is in the span**.

---

### **3. Finding the Value of an Unknown Such That a Vector Lies in the Span**

You may be given an **unknown component** in the target vector or among the scalars and asked to solve for it such that the linear combination holds.

---

#### **Example:**

$`\text{Find } a \text{ so that } \mathbf{b} = \begin{bmatrix} a \\ 4 \end{bmatrix} \in \text{Span}\left\{ \begin{bmatrix} 1 \\ 2 \end{bmatrix}, \begin{bmatrix} 3 \\ -1 \end{bmatrix} \right\}`$

Let:

$`x_1\begin{bmatrix} 1 \\ 2 \end{bmatrix} + x_2\begin{bmatrix} 3 \\ -1 \end{bmatrix} = \begin{bmatrix} a \\ 4 \end{bmatrix} \Rightarrow \begin{cases} x_1 + 3x_2 = a \\2x_1 - x_2 = 4 \end{cases}`$


Solve second equation: $`x_2 = 2x_1 - 4`$


Substitute into the first:

$`x_1 + 3(2x_1 - 4) = a \Rightarrow x_1 + 6x_1 - 12 = a \Rightarrow 7x_1 - 12 = a`$

You now have a **relation** for $a$; for any $x_1$, this determines an $a$ such that $`\mathbf{b}`$ lies in the span.

---

### **4. Determining Whether a Vector Lies on a Plane**

If a plane is defined by two spanning vectors $`\mathbf{v}_1`$ and $`\mathbf{v}_2`$, and a point $`\mathbf{p}_0`$, then vector $`\mathbf{b}`$ lies on the plane if:

$`\mathbf{b} = \mathbf{p}_0 + s\mathbf{v}_1 + t\mathbf{v}_2`$

Or equivalently, $`\mathbf{b} - \mathbf{p}_0 \in \text{Span}\{\mathbf{v}_1, \mathbf{v}_2\}`$

---

#### **Example:**

Let plane pass through $`(1, 0, 2)`$ with spanning vectors:

* $`\mathbf{v}_1 = \langle 1, 2, 0 \rangle`$


* $`\mathbf{v}_2 = \langle 0, 1, 3 \rangle`$

Check if point $(2, 3, 8)$ lies on the plane.

Compute:

$`\mathbf{b} - \mathbf{p}_0 = \langle 2, 3, 8 \rangle - \langle 1, 0, 2 \rangle = \langle 1, 3, 6 \rangle`$

Try solving:

$`s\langle 1, 2, 0 \rangle + t\langle 0, 1, 3 \rangle = \langle 1, 3, 6 \rangle`$

$`\Rightarrow \begin{cases} s = 1 \\2s + t = 3 \Rightarrow 2 + t = 3 \Rightarrow t = 1 \\3t = 6 \Rightarrow t = 2 \quad \text{(Contradiction!)} \end{cases}`$

So the system is **inconsistent**, meaning the point **does not lie on the plane**.

---

### Summary Table

| Task                                | Method                                                                           |
| ----------------------------------- | -------------------------------------------------------------------------------- |
| Check if a vector lies in a span    | Solve $`A\mathbf{x} = \mathbf{b}`$                                                 |
| Find unknown so vector lies in span | Substitute known values into the linear system                                   |
| Check if a vector lies on a plane   | Verify $`\mathbf{b} - \mathbf{p}_0 \in \text{Span}\{\mathbf{v}_1, \mathbf{v}_2\}`$ |

---

### **Conclusion**

The **span** concept is essential for understanding:

* Whether vectors form a **basis**


* The **dimension** of a space


* Whether a solution exists to a linear system


* Whether vectors lie on a **line, plane, or higher-dimensional surface**


It connects deeply to vector spaces, matrices, and real-world geometric reasoning.
