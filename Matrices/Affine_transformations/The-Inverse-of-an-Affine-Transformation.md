## **The Inverse of an Affine Transformation**

An **affine transformation** maps points using a combination of linear transformation and translation:

$$
T(\mathbf{x}) = A\mathbf{x} + \mathbf{b}
$$

Its **inverse** (when it exists) undoes this transformation, mapping the transformed output back to the original input:

$$
T^{-1}(\mathbf{y}) = A^{-1}(\mathbf{y} - \mathbf{b})
$$

---

### **1. Identifying Invertible Affine Transformations**

An affine transformation $`T(\mathbf{x}) = A\mathbf{x} + \mathbf{b}`$ is **invertible** **if and only if** the matrix $`A`$ is **invertible**.

#### ✅ To be invertible:

* $`\det(A) \neq 0`$


* $`A^{-1}`$ exists


* The transformation is **non-degenerate** (does not collapse space)

---


### **2. Inverting Affine Transformations Given in Matrix Form**

Given:

$$
T(\mathbf{x}) = A\mathbf{x} + \mathbf{b}
$$

To find the inverse $`T^{-1}`$, solve for $`\mathbf{x}`$:

$$
\mathbf{y} = A\mathbf{x} + \mathbf{b} \Rightarrow \mathbf{x} = A^{-1}(\mathbf{y} - \mathbf{b})
$$

#### **Example:**

Let

$$
A = \begin{bmatrix} 2 & 1 \\ 0 & 3 \end{bmatrix}, \quad \mathbf{b} = \begin{bmatrix} 1 \\ -2 \end{bmatrix}
$$


Then:

* Compute $`A^{-1}`$:

$$
A^{-1} = \begin{bmatrix} \frac{1}{2} & -\frac{1}{6} \\ 0 & \frac{1}{3} \end{bmatrix}
$$

* Apply the formula:

$$
T^{-1}(\mathbf{y}) = A^{-1}(\mathbf{y} - \mathbf{b})
$$

---

### **3. Inverting Affine Transformations Given in Parametric Form**

If the affine transformation is given as:

$$
T(x, y) = (ax + by + c,\ dx + ey + f)
$$

Then:

1. Express it in matrix form:

$$
T(\mathbf{x}) = A\mathbf{x} + \mathbf{b}
$$

2. Find $`A^{-1}`$, and apply:

$$
T^{-1}(\mathbf{y}) = A^{-1}(\mathbf{y} - \mathbf{b})
$$

#### **Example:**

Given:

$$
T(x, y) = (2x + y + 3,\ x + 3y - 1)
$$

Then:

* $`A = \begin{bmatrix} 2 & 1 \\ 1 & 3 \end{bmatrix}`$


* $`\mathbf{b} = \begin{bmatrix} 3 \\ -1 \end{bmatrix}`$

Use matrix inversion and subtraction to find $`T^{-1}`$.

---

### **4. Identifying the Types of Images Formed by an Affine Transformation**

Affine transformations **preserve**:

* **Lines and segments**


* **Parallelism**


* **Ratios of distances along parallel lines**


They **do not necessarily preserve**:

* Angles
* Lengths
* Areas (unless determinant = ±1)


#### **Types of images** (based on the transformation):

* If $`\det(A) > 0`$: orientation preserved


* If $`\det(A) < 0`$: orientation reversed (reflection included)


* If $`|\det(A)| = 1`$: area preserved


* If $`|\det(A)| \neq 1`$: shape is distorted (scaled or sheared)

---

### ✅ **Summary Table**

| Task                     | Description                                                     |
| ------------------------ | --------------------------------------------------------------- |
| **Invertibility**        | $`\det(A) \neq 0 \Rightarrow A^{-1}`$ exists                      |
| **Inverse formula**      | $`T^{-1}(\mathbf{y}) = A^{-1}(\mathbf{y} - \mathbf{b})`$          |
| **From parametric form** | Convert to matrix + vector, invert                              |
| **Types of images**      | Lines → lines, parallelism preserved, angles/lengths may change |

---


### **Conclusion**

The inverse of an affine transformation **reverses its geometric effect**, allowing us to trace 
transformed points back to their origins. Mastering this process is critical in fields such as 
robotics, graphics, and optimization, where transformations and their reversals are foundational 
to analysis and control.
