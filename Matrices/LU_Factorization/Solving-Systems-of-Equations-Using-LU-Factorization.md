**Solving Systems of Equations Using LU Factorization, Deep Dive**

LU factorization is a powerful method in numerical linear algebra for solving systems of equations of the form:

$$
A \mathbf{x} = \mathbf{b}
$$

If \$A\$ can be factored as \$A = LU\$, where \$L\$ is a lower triangular matrix and \$U\$ is an upper triangular matrix, then the system becomes:

$$
LU \mathbf{x} = \mathbf{b}
$$

This can be solved in two stages:

1. Solve the **intermediate system**: \$L\mathbf{y} = \mathbf{b}\$ (forward substitution)
2. Then solve: \$U\mathbf{x} = \mathbf{y}\$ (back substitution)

---

### 🔹 General Procedure for LU-Based Solution

Given: \$A \mathbf{x} = \mathbf{b}\$

1. **LU Factorization**: Write \$A = LU\$
2. **Forward Substitution**: Solve \$L \mathbf{y} = \mathbf{b}\$ for \$\mathbf{y}\$
3. **Backward Substitution**: Solve \$U \mathbf{x} = \mathbf{y}\$ for \$\mathbf{x}\$

---

### 🔹 Finding the Solution of an Intermediate System Using LU Factorization of a 2x2 Matrix

Let:

$$
A = \begin{bmatrix} 2 & 3 \\ 4 & 7 \end{bmatrix},\quad \mathbf{b} = \begin{bmatrix} 5 \\ 11 \end{bmatrix}
$$

LU factorization gives:

$$
L = \begin{bmatrix} 1 & 0 \\ 2 & 1 \end{bmatrix},\quad
U = \begin{bmatrix} 2 & 3 \\ 0 & 1 \end{bmatrix}
$$

**Step 1: Solve** \$L\mathbf{y} = \mathbf{b}\$

$$
\begin{aligned}
1 \cdot y_1 + 0 \cdot y_2 &= 5 \Rightarrow y_1 = 5 \\
2 \cdot y_1 + 1 \cdot y_2 &= 11 \Rightarrow y_2 = 11 - 2 \cdot 5 = 1
\end{aligned}
$$

So, \$\mathbf{y} = \begin{bmatrix} 5 \ 1 \end{bmatrix}\$

**Step 2: Solve** \$U\mathbf{x} = \mathbf{y}\$

$$
\begin{aligned}
2x_1 + 3x_2 &= 5 \\
x_2 &= 1
\end{aligned}
\Rightarrow x_1 = \frac{5 - 3 \cdot 1}{2} = 1
$$

Final solution:

$$
\mathbf{x} = \begin{bmatrix} 1 \\ 1 \end{bmatrix}
$$

---

### 🔹 Finding the Solution of an Intermediate System Using LU Factorization of a 3x3 Matrix

Let:

$$
A = \begin{bmatrix}
2 & 4 & 1 \\
4 & 9 & 3 \\
2 & 3 & 2
\end{bmatrix},\quad
\mathbf{b} = \begin{bmatrix}
3 \\ 8 \\ 4
\end{bmatrix}
$$

LU factorization gives:

$$
L = \begin{bmatrix}
1 & 0 & 0 \\
2 & 1 & 0 \\
1 & -1 & 1
\end{bmatrix},\quad
U = \begin{bmatrix}
2 & 4 & 1 \\
0 & 1 & 1 \\
0 & 0 & 2
\end{bmatrix}
$$

**Step 1: Solve** \$L\mathbf{y} = \mathbf{b}\$

$$
\begin{aligned}
y_1 &= 3 \\
2y_1 + y_2 &= 8 \Rightarrow y_2 = 8 - 6 = 2 \\
y_1 - y_2 + y_3 &= 4 \Rightarrow y_3 = 4 - 3 + 2 = 3
\end{aligned}
\Rightarrow \mathbf{y} = \begin{bmatrix} 3 \\ 2 \\ 3 \end{bmatrix}
$$

**Step 2: Solve** \$U\mathbf{x} = \mathbf{y}\$

$$
\begin{aligned}
2x_1 + 4x_2 + 1x_3 &= 3 \\
1x_2 + 1x_3 &= 2 \\
2x_3 &= 3
\end{aligned}
\Rightarrow x_3 = 1.5,\quad x_2 = 2 - 1.5 = 0.5,\quad x_1 = \frac{3 - 4(0.5) - 1.5}{2} = -0.25
$$

Final solution:

$$
\mathbf{x} = \begin{bmatrix} -0.25 \\ 0.5 \\ 1.5 \end{bmatrix}
$$

---

### 🔹 Solving a 2x2 Linear System Using LU Factorization

**Given:**

$$
A = \begin{bmatrix} 1 & 2 \\ 3 & 8 \end{bmatrix},\quad \mathbf{b} = \begin{bmatrix} 5 \\ 17 \end{bmatrix}
$$

**Step 1: LU Factorization**

$$
L = \begin{bmatrix} 1 & 0 \\ 3 & 1 \end{bmatrix},\quad
U = \begin{bmatrix} 1 & 2 \\ 0 & 2 \end{bmatrix}
$$

**Step 2: Solve** \$L\mathbf{y} = \mathbf{b}\$

$$
y_1 = 5,\quad 3y_1 + y_2 = 17 \Rightarrow y_2 = 17 - 15 = 2
$$

**Step 3: Solve** \$U\mathbf{x} = \mathbf{y}\$

$$
2x_2 = 2 \Rightarrow x_2 = 1,\quad x_1 + 2x_2 = 5 \Rightarrow x_1 = 3
$$

**Final Answer:**

$$
\mathbf{x} = \begin{bmatrix} 3 \\ 1 \end{bmatrix}
$$

---

### ✅ Summary Table

| Step                  | Purpose                            | Method               |
| --------------------- | ---------------------------------- | -------------------- |
| LU Factorization      | Decompose \$A\$ into \$LU\$        | Gaussian Elimination |
| Forward Substitution  | Solve \$L\mathbf{y} = \mathbf{b}\$ | Bottom-up solving    |
| Backward Substitution | Solve \$U\mathbf{x} = \mathbf{y}\$ | Top-down solving     |

This method simplifies solving multiple systems with the same \$A\$ but different \$\mathbf{b}\$ vectors by reusing the LU decomposition.
