## **Linear Combinations of Vectors in N-Dimensional Euclidean Space**

In $\mathbb{R}^n$, a **linear combination** of vectors involves **scaling** and **adding** vectors 
together. It forms the backbone of vector spaces, systems of equations, span, and linear dependence.

---

### **1. Definition of a Linear Combination**

Given vectors $\mathbf{v}_1, \mathbf{v}_2, \dots, \mathbf{v}_k \in \mathbb{R}^n$ and scalars $c_1, c_2, \dots, c_k \in \mathbb{R}$, the expression:

$$
c_1\mathbf{v}_1 + c_2\mathbf{v}_2 + \dots + c_k\mathbf{v}_k
$$

is called a **linear combination** of the vectors $\mathbf{v}_i$.

---

### **2. Geometric Interpretation**

* In $\mathbb{R}^2$: linear combinations of two non-parallel vectors span a **plane**.


* In $\mathbb{R}^3$: three linearly independent vectors span the entire **space**.


* The **span** of a set of vectors is the collection of all their linear combinations.

---

### **3. Solving for One Coefficient in a Linear Combination**

If all other coefficients are known, isolate the unknown.

#### **Example:**

Given $2\mathbf{v}_1 + c\mathbf{v}_2 = \mathbf{b}$, and known vectors, subtract $2\mathbf{v}_1$ from both sides:

$$
c\mathbf{v}_2 = \mathbf{b} - 2\mathbf{v}_1 \Rightarrow c = \frac{\text{componentwise}}{\mathbf{v}_2}
$$

---

### **4. Solving for a Vector in a Linear Combination**

You may solve for an unknown vector when coefficients and the result vector are known.

#### **Example:**

$$
3\mathbf{v} + 2\begin{bmatrix} 1 \\ -1 \end{bmatrix} = \begin{bmatrix} 5 \\ 1 \end{bmatrix}
\Rightarrow
3\mathbf{v} = \begin{bmatrix} 5 \\ 1 \end{bmatrix} - \begin{bmatrix} 2 \\ -2 \end{bmatrix} = \begin{bmatrix} 3 \\ 3 \end{bmatrix}
\Rightarrow \mathbf{v} = \begin{bmatrix} 1 \\ 1 \end{bmatrix}
$$

---

### **5. Solving for Two Coefficients in a Linear Combination**

You’re given:

$$
x_1\mathbf{v}_1 + x_2\mathbf{v}_2 = \mathbf{b}
$$

Write the equation as a system of equations and solve using **substitution** or **elimination**.

#### **Example:**

Let:

* $`\mathbf{v}_1 = \begin{bmatrix} 1 \\ 2 \end{bmatrix}`$
* $`\mathbf{v}_2 = \begin{bmatrix} 3 \\ -1 \end{bmatrix}`$
* $`\mathbf{b} = \begin{bmatrix} 9 \\ 1 \end{bmatrix}`$

Then:

$$
x_1 + 3x_2 = 9 \quad \text{(1)} \\
2x_1 - x_2 = 1 \quad \text{(2)}
$$

Solve (1) and (2) simultaneously:

From (1): $x_1 = 9 - 3x_2$

Substitute into (2):

$$
2(9 - 3x_2) - x_2 = 1 \Rightarrow 18 - 6x_2 - x_2 = 1 \Rightarrow 7x_2 = 17 \Rightarrow x_2 = \frac{17}{7}, \quad x_1 = 9 - 3 \cdot \frac{17}{7} = \frac{12}{7}
$$

---

### **6. Solving for Three Coefficients in a Linear Combination**

Given:

$$
x_1\mathbf{v}_1 + x_2\mathbf{v}_2 + x_3\mathbf{v}_3 = \mathbf{b}
$$

Write this as a **system of 3 equations in 3 variables** and solve using **matrix methods (Gaussian elimination, inverse matrices)**.

#### **Example:**

Let:

* $`\mathbf{v}_1 = \begin{bmatrix} 1 \\ -1 \\ 2 \end{bmatrix}, \quad \mathbf{v}_2 = \begin{bmatrix} 4 \\ -3 \\ 8 \end{bmatrix}, \quad \mathbf{v}_3 = \begin{bmatrix} 7 \\ -7 \\ 14 \end{bmatrix}`$

* $`\mathbf{b} = \begin{bmatrix} 5 \\ -3 \\ 7 \end{bmatrix}`$

Set up:

$`\begin{bmatrix}  1 & 4 & 7 \\ -1 & -3 & -7 \\ 2 & 8 & 14  \end{bmatrix}  \begin{bmatrix}  x_1 \\ x_2 \\ x_3  \end{bmatrix} =  \begin{bmatrix}  5 \\ -3 \\ 7  \end{bmatrix}`$

Solve using **row operations** or substitution techniques. If one vector is a linear combination of the others, reduce the system accordingly.

---

### Summary Table

| Goal               | Method                                                    |
| ------------------ | --------------------------------------------------------- |
| One coefficient    | Isolate variable after rearranging                        |
| One vector         | Solve vector equation component-wise                      |
| Two coefficients   | Solve 2×2 system (substitution/elimination)               |
| Three coefficients | Solve 3×3 system (Gaussian elimination or matrix inverse) |

---

### **Conclusion**

Linear combinations in $\mathbb{R}^n$ allow you to:

* Understand **vector span** and **basis**,
* Solve **vector equations** systematically,
* Determine **linear independence** and **dimensionality** of a space.

They are the core of linear algebra and fundamental to systems, transformations, and projections.
