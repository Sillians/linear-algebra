## **The Cauchy–Schwarz Inequality and the Angle Between Two Vectors**

The **Cauchy–Schwarz inequality** is a fundamental result in vector algebra and analysis. 
It bounds the dot product of two vectors by the product of their magnitudes and plays a 
crucial role in defining the **angle between two vectors** in Euclidean space.

---

### **1. The Cauchy–Schwarz Inequality**

For any vectors $\mathbf{u}, \mathbf{v} \in \mathbb{R}^n$:

$$
\boxed{|\mathbf{u} \cdot \mathbf{v}| \leq \|\mathbf{u}\| \cdot \|\mathbf{v}\|}
$$

Equality holds **if and only if** $`\mathbf{u}`$ and $`\mathbf{v}`$ are **linearly dependent** (i.e., one is a scalar multiple of the other).

---

### **2. Determining a Minimum Possible Value Using the Cauchy–Schwarz Inequality**

If you're given the magnitudes of two vectors, the **minimum value** of the dot product is:

$$
\boxed{\mathbf{u} \cdot \mathbf{v} \geq -\|\mathbf{u}\| \cdot \|\mathbf{v}\|}
$$

The **dot product** achieves its minimum when the vectors point in **opposite directions** (angle = 180°, $\cos\theta = -1$).

#### **Example:**

Let $`\|\mathbf{u}\| = 4`$, $`\|\mathbf{v}\| = 3`$

Then:

* **Maximum dot product**: $`4 \cdot 3 = 12`$


* **Minimum dot product**: $`-4 \cdot 3 = -12`$

---

### **3. Finding the Acute Angle Between Two Vectors**

Given two nonzero vectors $`\mathbf{u}`$ and $`\mathbf{v}`$, the **angle $\theta$** between them is defined by:

$$
\boxed{\cos\theta = \frac{\mathbf{u} \cdot \mathbf{v}}{\|\mathbf{u}\| \cdot \|\mathbf{v}\|}}
\quad \text{where } 0 \leq \theta \leq \pi
$$

Use the inverse cosine to find the angle:

$$
\boxed{\theta = \cos^{-1} \left( \frac{\mathbf{u} \cdot \mathbf{v}}{\|\mathbf{u}\| \cdot \|\mathbf{v}\|} \right)}
$$

---

#### **Example:**

Let $`\mathbf{u} = \langle 2, 1 \rangle`$, $`\mathbf{v} = \langle 1, 3 \rangle`$

* $`\mathbf{u} \cdot \mathbf{v} = (2)(1) + (1)(3) = 5`$


* $`\|\mathbf{u}\| = \sqrt{2^2 + 1^2} = \sqrt{5}`$


* $`\|\mathbf{v}\| = \sqrt{1^2 + 3^2} = \sqrt{10}`$

Then:

$$
\cos\theta = \frac{5}{\sqrt{5} \cdot \sqrt{10}} = \frac{5}{\sqrt{50}} = \frac{5}{5\sqrt{2}} = \frac{1}{\sqrt{2}} \Rightarrow \theta = \cos^{-1}\left( \frac{1}{\sqrt{2}} \right) = 45^\circ
$$

---

### **4. Calculating the Cosine of an Angle Between Two Vectors**

The cosine gives a **measure of alignment**:

* $`\cos\theta = 1 \Rightarrow \theta = 0^\circ`$ (vectors point in the same direction)


* $`\cos\theta = 0 \Rightarrow \theta = 90^\circ`$ (vectors are orthogonal)


* $`\cos\theta = -1 \Rightarrow \theta = 180^\circ`$ (vectors point in opposite directions)


Again, use:

$$
\boxed{\cos\theta = \frac{\mathbf{u} \cdot \mathbf{v}}{\|\mathbf{u}\|\|\mathbf{v}\|}}
$$

---

### ✅ **Summary Table**
| Task                      | Formula                                                                                              |                                          
| ------------------------- |------------------------------------------------------------------------------------------------------|  
| Cauchy–Schwarz Inequality | $`(\mid \mathbf{u} \cdot \mathbf{v} \mid \leq \|\mathbf{u}\|\|\mathbf{v}\| )`$                       |
| Minimum dot product       | $-\|\mathbf{u}\|\|\mathbf{v}\|$                                                                      |                                                          
| Cosine of angle           | $\cos\theta = \dfrac{\mathbf{u} \cdot \mathbf{v}}{\|\mathbf{u}\|\|\mathbf{v}\|}$                     |                                                           
| Angle between vectors     | $\theta = \cos^{-1} \left( \frac{\mathbf{u} \cdot \mathbf{v}}{\|\mathbf{u}\|\|\mathbf{v}\|} \right)$ |                             

---

### **Conclusion**

The Cauchy–Schwarz inequality is not only a bound on the dot product, but a key tool for 
measuring **alignment**, determining **angle**, and verifying **dependence** between vectors. 
Combined with cosine calculations, it lets you quantify direction and angle precisely in $`\mathbb{R}^n`$.
