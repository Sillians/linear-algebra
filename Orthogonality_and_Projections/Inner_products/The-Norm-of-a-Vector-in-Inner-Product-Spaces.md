## **The Norm of a Vector in Inner Product Spaces**

---

### **Overview**

In an **inner product space** $`V`$, the **norm** of a vector $`v \in V`$ is a measure of its “length” and is induced by the inner product. 
The norm generalizes the concept of Euclidean length to more abstract vector spaces, including spaces of polynomials, continuous functions, and complex-valued vectors.


The **norm** $`\|v\|`$ of a vector $`v`$ is defined as:


$`\|v\| = \sqrt{\langle v, v \rangle}`$


where $`\langle \cdot, \cdot \rangle`$ is the inner product on $`V`$.

---

### **1. Calculating the Norm of a Vector With Respect to a Given Inner Product**

Let $V$ be an inner product space with inner product $`\langle \cdot, \cdot \rangle`$, and let $`v \in V`$. 
The norm is computed by:


$`\|v\| = \sqrt{\langle v, v \rangle}`$


**Example**:

In $`\mathbb{R}^2`$, with standard dot product:


$`v = \begin{bmatrix} 3 \\ 4 \end{bmatrix},\quad \langle v, v \rangle = 3^2 + 4^2 = 25 \Rightarrow \|v\| = \sqrt{25} = 5`$

---

### **2. Calculating the Norm of a Vector in an Inner Product Space of Polynomials**


Let $`V = \mathbb{P}_n`$, the space of real polynomials of degree at most $`n`$, with inner product:


$`\langle f, g \rangle = \int_a^b f(x)g(x)\,dx`$


**Example**:


Let $`f(x) = 1 + x \in \mathbb{P}_1`$, and the inner product is over $`[0,1]`$:


$`\|f\| = \sqrt{\int_0^1 (1 + x)^2\, dx} = \sqrt{\int_0^1 (1 + 2x + x^2)\, dx}`$


$`= \sqrt{1 + 1 + \frac{1}{3}} = \sqrt{\frac{7}{3}} \approx 1.53`$


---

### **3. Calculating the Norm of a Vector in an Inner Product Space of Continuous Functions**

Let $`V = C[a,b]`$, the space of continuous functions on $`[a,b]`$, with:


$`\langle f, g \rangle = \int_a^b f(x)g(x)\,dx`$


**Example**:


Let $`f(x) = \cos(x)`$, over $`[0, \pi]`$:


$`\|f\| = \sqrt{\int_0^\pi \cos^2(x)\, dx} = \sqrt{\frac{\pi}{2}}`$


(since $`\cos^2(x) = \frac{1 + \cos(2x)}{2}`$ and the integral simplifies)

---

### **4. Normalizing a Vector in an Inner Product Space**

A vector $`v \in V`$ is **normalized** by dividing it by its norm:


$`u = \frac{v}{\|v\|} \quad \text{such that} \quad \|u\| = 1`$

**Example**:


Let $`v = \begin{bmatrix} 6 \\ 8 \end{bmatrix}`$, then:


$`\|v\| = \sqrt{6^2 + 8^2} = 10,\quad u = \frac{1}{10} \begin{bmatrix} 6 \\ 8 \end{bmatrix} = \begin{bmatrix} 0.6 \\ 0.8 \end{bmatrix}`$

---

### **Summary Table**

| Context                            | Inner Product                                            | Norm Formula                            |
|------------------------------------|----------------------------------------------------------|-----------------------------------------|
| Euclidean Space $`\mathbb{R}^n`$   | $`\langle \mathbf{u}, \mathbf{v} \rangle = \sum u_iv_i`$ | $`\|\mathbf{v}\| = \sqrt{\sum v_i^2}`$  |
| Polynomial Space $`\mathbb{P}_n`$  | $`\langle f, g \rangle = \int_a^b f(x)g(x)\, dx`$        | $`\|f\| = \sqrt{\int_a^b f(x)^2\, dx}`$ |
| Continuous Functions $`C[a,b]`$    | Same as above                                            | Same as above                           |
| General Inner Product Space        | $`\langle v, v \rangle`$ defined appropriately           | $`\|v\| = \sqrt{\langle v, v \rangle}`$ |

---

The norm in inner product spaces generalizes geometric length and underpins many concepts in functional analysis, numerical analysis, and quantum mechanics.
