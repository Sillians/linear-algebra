## **The Conditional Definition of a Set**

A **conditionally defined set** is a collection of elements that satisfy a **specific rule or condition**. 
Rather than listing elements explicitly, the set is defined by the **properties** its elements must meet.

It is typically written in **set-builder notation**:

$$
A = \{ x \in S \mid \text{condition on } x \}
$$

Where:

* $`S`$ is the **universal set** or domain of interest
* The condition defines which elements from $`S`$ are **included** in the set

---

### **1. Sets Defined Using Linear Equations and Inequalities**

These sets include elements that satisfy a **linear condition**, such as:

$$
A = \{ x \in \mathbb{R} \mid 2x - 3 = 7 \}
\Rightarrow A = \{5\}
$$

$$
B = \{ x \in \mathbb{Z} \mid 4x + 1 \leq 17 \}
\Rightarrow B = \{ x \in \mathbb{Z} \mid x \leq 4 \}
\Rightarrow B = \{\ldots, 1, 0, -1, -2, -3, -4\}
$$

These can also define **intervals** or **specific integer values**.

---

### **2. Sets Defined Using Quadratic Equations and Inequalities**

These involve conditions based on quadratic expressions:

$$
C = \{ x \in \mathbb{R} \mid x^2 - 4x + 3 = 0 \}
\Rightarrow C = \{1, 3\}
$$

$$
D = \{ x \in \mathbb{R} \mid x^2 \leq 9 \}
\Rightarrow D = [-3, 3]
$$

Quadratic inequalities often define **intervals** on the real line.

---

### **3. Sets Defined Using Absolute Value Equations and Inequalities**

Absolute value conditions describe symmetry around a point:

$$
E = \{ x \in \mathbb{R} \mid |x - 2| \leq 5 \}
\Rightarrow -5 \leq x - 2 \leq 5 \Rightarrow -3 \leq x \leq 7
\Rightarrow E = [-3, 7]
$$

$$
F = \{ x \in \mathbb{Z} \mid |2x + 1| = 3 \}
\Rightarrow 2x + 1 = \pm 3 \Rightarrow x = 1, -2
\Rightarrow F = \{-2, 1\}
$$

These sets are useful for defining **bounded ranges** or **symmetric sets**.

---

### **4. Sets Defined Using Trigonometric Equations**

Trigonometric sets include solutions to sine, cosine, or tangent conditions over a domain:

$$
G = \{\theta \in [0, 2\pi] \mid \sin(\theta) = 1/2\}
\Rightarrow G = \{\pi/6, 5\pi/6\}
$$



$$
H = \{\, x \in \mathbb{R} \mid \cos(x) = 0 \,\}
\Rightarrow H = \{\, \tfrac{\pi}{2} + n\pi \mid n \in \mathbb{Z} \,\}
$$

These are often **periodic** sets with infinite elements.

---

### ✅ Summary Table

| Condition Type | Example                                   | Resulting Set        |          
| -------------- |-------------------------------------------|----------------------| 
| Linear         | $`\{x \in \mathbb{Z} \mid 3x + 1 = 10\}`$ | $`\{3\}`$            |          
| Quadratic      | $`\{x \in \mathbb{R} \mid x^2 < 16\}`$    | $`(-4, 4)`$          |           
| Absolute Value | $`( {x \in \mathbb{R} \mid x \leq 2} )`$  | $[-2, 2]$            |
| Trigonometric  | $`\{x \in [0, 2\pi] \mid \sin(x) = 0 \}`$ | $`\{0, \pi, 2\pi\}`$ |           

---

### **Conclusion**

Conditionally defined sets allow you to **express infinite or complex sets** compactly using mathematical rules. 
They are fundamental in algebra, calculus, and advanced mathematics, and they provide a powerful way to define domains, 
constraints, and solutions across all mathematical fields.
