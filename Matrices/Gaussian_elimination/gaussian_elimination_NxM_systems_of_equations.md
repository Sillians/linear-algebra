## **Gaussian Elimination for $N \times M$ Systems of Equations**

---

### **1. What Is Gaussian Elimination?**

**Gaussian Elimination** is a method for solving systems of linear equations by converting the augmented matrix of the system into **row echelon form (REF)** using **elementary row operations**.

Once in REF, **back-substitution** is used to solve for the unknown variables.

It applies to systems of equations represented as:

$$
A\mathbf{x} = \mathbf{b}
$$

Where:

* $A$ is an $N \times M$ matrix of coefficients,


* $`\mathbf{x}`$ is a vector of unknowns (length $M$),


* $`\mathbf{b}`$ is a vector of constants (length $N$).

---

### **2. Elementary Row Operations**

Gaussian elimination uses three allowed operations:

* **Swap** two rows.


* **Scale** a row by a non-zero constant.


* **Add or subtract** a multiple of one row to another row.


These operations do not change the solution set.

---

### **3. The Goal: Row Echelon Form (REF)**

A matrix is in **row echelon form** if:

* All nonzero rows are above any rows of all zeros.


* The leading entry (pivot) in each row is to the right of the pivot in the row above.


* All entries below a pivot are zero.

**Reduced Row Echelon Form (RREF)** goes further by making all entries **above** each pivot zero, and all pivots equal to 1. RREF is used in **Gauss–Jordan elimination**, not basic Gaussian elimination.

---

### **4. Solving a System via Gaussian Elimination: Step-by-Step**

#### Example System:

$$
\begin{aligned}
x + 2y + z &= 6 \\
2x + 5y + z &= -4 \\
4x + 10y + 2z &= -8
\end{aligned}
$$

**Step 1: Convert to Augmented Matrix**

$$
\left[\begin{array}{ccc|c}
1 & 2 & 1 & 6 \\
2 & 5 & 1 & -4 \\
4 & 10 & 2 & -8
\end{array}\right]
$$

**Step 2: Use row operations to create zeros below the pivot in column 1**

* Replace Row 2 with (Row 2 - 2 × Row 1):

$$
R_2 = [2,5,1,-4] - 2 \cdot [1,2,1,6] = [0,1,-1,-16]
$$

* Replace Row 3 with (Row 3 - 4 × Row 1):

$$
R_3 = [4,10,2,-8] - 4 \cdot [1,2,1,6] = [0,2,-2,-32]
$$

Now:

$$
\left[\begin{array}{ccc|c}
1 & 2 & 1 & 6 \\
0 & 1 & -1 & -16 \\
0 & 2 & -2 & -32
\end{array}\right]
$$

**Step 3: Eliminate below the pivot in column 2**

* Replace Row 3 with (Row 3 - 2 × Row 2):

$$
R_3 = [0,2,-2,-32] - 2 \cdot [0,1,-1,-16] = [0,0,0,0]
$$

Now:

$$
\left[\begin{array}{ccc|c}
1 & 2 & 1 & 6 \\
0 & 1 & -1 & -16 \\
0 & 0 & 0 & 0
\end{array}\right]
$$

This is **Row Echelon Form**.

---

### **5. Back-Substitution**

From the matrix:

$$
\begin{aligned}
x + 2y + z &= 6 \\
y - z &= -16
\end{aligned}
$$

Let’s solve from bottom to top:

* From the second equation: $y = -16 + z$
* Substitute into the first:

$$
x + 2(-16 + z) + z = 6 \Rightarrow x - 32 + 2z + z = 6 \Rightarrow x + 3z = 38 \Rightarrow x = 38 - 3z
$$

Thus, the **general solution** is:

$$
x = 38 - 3z, \quad y = -16 + z, \quad z = z \text{ (free variable)}
$$

Or:

$` \begin{bmatrix}  x \\ y \\ z  \end{bmatrix} =  \begin{bmatrix}  38 \\ -16 \\ 0  \end{bmatrix} + z \cdot  \begin{bmatrix}  -3 \\ 1 \\ 1  \end{bmatrix} `$

---

### **6. When Does Gaussian Elimination Work?**

* Works for **square** and **rectangular** systems.
* Can detect **inconsistent systems** (e.g., a row like $[0\ 0\ 0\ |\ c]$ with $c \neq 0$).
* Can find **unique**, **infinite**, or **no solutions**.

---

### **7. Summary**

* **Gaussian Elimination** transforms a system to row echelon form using row operations.
* It simplifies solving systems via **back-substitution**.
* It applies to **$N \times M$** systems: square or rectangular.
* Handles consistent, inconsistent, and underdetermined systems.
* Forms the basis for **matrix inversion**, **rank determination**, and **LU decomposition**.

This is one of the most fundamental algorithms in linear algebra and computational mathematics.










### **Determining the Value of a Constant for Consistency in Gaussian Elimination**

---

### **1. What Does It Mean for a System to Be Consistent?**

A **linear system is consistent** if it has **at least one solution** (either unique or infinitely many). It is **inconsistent** if **no solution** exists.

When solving systems via **Gaussian elimination**, **inconsistency** appears when you reach a row like:

$`0x + 0y + 0z = c \quad \text{(where \( c \neq 0 \))}`$

This is a contradiction (e.g., $0 = 5$) and means **no solution** exists.

---

### **2. Strategy for Determining the Value of a Constant**

Given a linear system that contains an **unknown constant parameter** (e.g., $k$), you can use Gaussian elimination to reduce the system and **identify the value(s) of $k$** for which:

* The system is **consistent** (no contradictory equation appears),


* The system is **inconsistent** (contradiction arises from some $k$).

---

### **3. Example Problem**

**Given:**

$$
\begin{aligned}
x + 2y + z &= 3 \\
2x + 3y + kz &= 7 \\
3x + 7y + (k + 1)z &= 13
\end{aligned}
$$

Determine values of $k$ for which the system is **consistent**.

---

### **4. Step 1: Write the Augmented Matrix**

$$
\left[\begin{array}{ccc|c}
1 & 2 & 1 & 3 \\
2 & 3 & k & 7 \\
3 & 7 & k + 1 & 13
\end{array}\right]
$$

---

### **5. Step 2: Use Gaussian Elimination**

**Eliminate below the pivot in column 1:**

* Row 2: $R_2 \leftarrow R_2 - 2R_1$

$$
[2, 3, k, 7] - 2 \cdot [1, 2, 1, 3] = [0, -1, k - 2, 1]
$$

* Row 3: $R_3 \leftarrow R_3 - 3R_1$

$$
[3, 7, k + 1, 13] - 3 \cdot [1, 2, 1, 3] = [0, 1, k - 2, 4]
$$

Now:

$$
\left[\begin{array}{ccc|c}
1 & 2 & 1 & 3 \\
0 & -1 & k - 2 & 1 \\
0 & 1 & k - 2 & 4
\end{array}\right]
$$

---

**Eliminate below pivot in column 2:**

* Row 3: $R_3 \leftarrow R_3 + R_2$

$$
[0, 1, k - 2, 4] + [0, -1, k - 2, 1] = [0, 0, 2(k - 2), 5]
$$

Now:

$$
\left[\begin{array}{ccc|c}
1 & 2 & 1 & 3 \\
0 & -1 & k - 2 & 1 \\
0 & 0 & 2(k - 2) & 5
\end{array}\right]
$$

---

### **6. Step 3: Determine Consistency**

We now look at the **third row**:

$$
0x + 0y + 2(k - 2)z = 5
$$

This equation becomes:

$$
2(k - 2)z = 5
$$

If $2(k - 2) = 0 \Rightarrow k = 2$, the equation becomes:

$$
0z = 5 \Rightarrow \text{Contradiction}
$$

So the system is **inconsistent when $k = 2$**.

---

### **7. Final Conclusion**

* The system is **inconsistent** when $k = 2$.


* The system is **consistent** for **all other values of $k \neq 2$**.

---

### **8. Summary**

* Use **Gaussian elimination** to reduce the system to row echelon form.
* Watch for rows like $[0\ 0\ 0\ |\ c]$ with $c \neq 0$: these signal **inconsistency**.
* Solve for the constant(s) that **lead to or avoid contradictions**.
* This method allows **parametric analysis** of systems involving symbolic constants.












### **Classifying a System Using Gaussian Elimination**

When solving a system of linear equations using **Gaussian elimination**, the system can be 
classified into one of the following categories:

---

### **1. Classifications of Linear Systems**

| Classification             | Meaning                   | Graphical Interpretation                              |
| -------------------------- | ------------------------- | ----------------------------------------------------- |
| **Consistent Independent** | One unique solution       | Lines/planes intersect at one point                   |
| **Consistent Dependent**   | Infinitely many solutions | Lines/planes coincide                                 |
| **Inconsistent**           | No solution               | Lines/planes do not intersect (parallel/incompatible) |

---

### **2. How to Classify a System in Gaussian Elimination**

Convert the augmented matrix to **Row Echelon Form (REF)** using **elementary row operations**, then check:

#### ✅ **Consistent Independent (Unique Solution)**

* The system has **as many pivot rows as variables** (full rank).


* No contradictory rows.


* The matrix reduces to an identity form.



#### ✅ **Consistent Dependent (Infinitely Many Solutions)**

* There is **at least one free variable** (i.e., a column without a pivot).


* No contradictory rows.


* The system has **fewer pivot rows than variables**, implying parameters.



#### ❌ **Inconsistent (No Solution)**

* The REF has a row like:

$`[0 \ 0 \ \dots \ 0 \ | \ c] \quad \text{where } c \ne 0`$

* This indicates a contradiction like $0 = 5$, meaning **no solution exists**.

---

### **3. Examples**

#### **Example 1: Consistent Independent**

System:

$$
\begin{aligned}
x + y &= 2 \\
2x + 3y &= 5
\end{aligned}
$$

Augmented matrix:

$$
\left[\begin{array}{cc|c}
1 & 1 & 2 \\
2 & 3 & 5
\end{array}\right]
$$

After Gaussian elimination:

$$
\left[\begin{array}{cc|c}
1 & 1 & 2 \\
0 & 1 & 1
\end{array}\right]
$$

Unique solution: $x = 1, y = 1$ ⇒ **Consistent Independent**

---

#### **Example 2: Consistent Dependent**

System:

$$
\begin{aligned}
x + y &= 2 \\
2x + 2y &= 4
\end{aligned}
$$

Augmented matrix:

$$
\left[\begin{array}{cc|c}
1 & 1 & 2 \\
2 & 2 & 4
\end{array}\right]
$$

Row reduction yields:

$$
\left[\begin{array}{cc|c}
1 & 1 & 2 \\
0 & 0 & 0
\end{array}\right]
$$

Infinitely many solutions (e.g., $x = 2 - y$) ⇒ **Consistent Dependent**

---

#### **Example 3: Inconsistent**

System:

$$
\begin{aligned}
x + y &= 2 \\
x + y &= 3
\end{aligned}
$$

Augmented matrix:

$$
\left[\begin{array}{cc|c}
1 & 1 & 2 \\
1 & 1 & 3
\end{array}\right]
$$

Row reduction:

$$
\left[\begin{array}{cc|c}
1 & 1 & 2 \\
0 & 0 & 1
\end{array}\right]
$$

Contradiction: $0 = 1$ ⇒ **Inconsistent**

---

### **4. Summary**

To classify a system using Gaussian elimination:

* Reduce the augmented matrix to **REF**.
* **Look for contradictions**: if found → **Inconsistent**.
* **Check number of pivots vs variables**:

  * Pivots = variables → **Consistent Independent**.
  * Pivots < variables and no contradiction → **Consistent Dependent**.

Gaussian elimination not only solves systems but also reveals their structure and consistency.















