## **Rotation-Scaling Matrices**

A **rotation-scaling matrix** combines two fundamental geometric transformations in the plane: **rotation** 
about the origin and **scaling** (uniform or non-uniform change in magnitude). These transformations are 
linear and can be represented using **$`2 \times 2`$ real matrices**.

---

### **1. Identifying Rotation-Scaling Matrices**

A **rotation-scaling matrix** $A$ can be written in one of two typical forms:


#### a. **Uniform Scaling + Rotation:**

$`A = r \begin{bmatrix} \cos \theta & -\sin \theta \\\sin \theta & \cos \theta \end{bmatrix}`$


* $`r`$ is the **scaling factor**.


* $`\theta`$ is the **angle of rotation**, counterclockwise.

This form **preserves angles** and **scales all vectors equally**.


#### b. **Non-Uniform Scaling + Rotation (via SVD or Diagonalization):**

If $A$ is not orthogonal, it may still represent rotation and scaling through:

$`A = R D R^{-1} \quad \text{(or)} \quad A = U \Sigma V^T`$

* $D$ or $`\Sigma`$ contains scale factors (possibly unequal).


* $R$, $U$, and $V$ involve rotation.

---


### **2. Constructing a Rotation-Scaling Matrix That Represents a Geometric Transformation**

**Given:**

* Rotate by angle $`\theta`$


* Scale by factor $r$ (same in all directions)


**Then:**


$`A = r \cdot \begin{bmatrix} \cos \theta & -\sin \theta \\\sin \theta & \cos \theta \end{bmatrix}`$


**Example:**
Rotate by $`45^\circ`$ and scale by $2$:

$`A = 2 \begin{bmatrix} \cos(45^\circ) & -\sin(45^\circ) \\\sin(45^\circ) & \cos(45^\circ)\end{bmatrix} = 2 \begin{bmatrix} \frac{\sqrt{2}}{2} & -\frac{\sqrt{2}}{2} \\\frac{\sqrt{2}}{2} & \frac{\sqrt{2}}{2} \end{bmatrix} = \begin{bmatrix} \sqrt{2} & -\sqrt{2} \\\sqrt{2} & \sqrt{2} \end{bmatrix}`$

---


### **3. Finding the Scale Factors and Angles of Rotation of Rotation-Scaling Matrices**

Given a **rotation-scaling matrix** $`A = r R(\theta)`$:

* **Scale factor $r$** is the **norm of the image of any unit vector**, e.g.,

$`r = \| A \mathbf{u} \| \quad \text{for} \quad \| \mathbf{u} \| = 1`$

* **Angle of rotation $`\theta`$** can be recovered by comparing with the standard rotation matrix:

$`R = \frac{1}{r} A = \begin{bmatrix} \cos \theta & -\sin \theta \\\sin \theta & \cos \theta \end{bmatrix}`$

Then,

$`\cos \theta = R_{11}, \quad \sin \theta = R_{21}`$

Ensure that $`\theta`$ satisfies the quadrant based on signs of $`\cos \theta`$ and $`\sin \theta`$.

**Example:**

Let

$`A = \begin{bmatrix} \sqrt{2} & -\sqrt{2} \\\sqrt{2} & \sqrt{2} \end{bmatrix}`$

Then

$`r = \| A \mathbf{e}_1 \| = \left\| \begin{bmatrix} \sqrt{2} \\ \sqrt{2} \end{bmatrix} \right\| = \sqrt{2^2 + 2^2} = 2`$

Now,

$`R = \frac{1}{2} A = \begin{bmatrix} \frac{\sqrt{2}}{2} & -\frac{\sqrt{2}}{2} \\\frac{\sqrt{2}}{2} & \frac{\sqrt{2}}{2} \end{bmatrix} \Rightarrow \theta = 45^\circ, \quad r = 2`$

---

### **4. Sketching the Image of a Vector Under the Action of a Rotation-Scaling Matrix**

**Step-by-step method:**

1. **Start with original vector** $`\mathbf{v}`$.


2. **Apply matrix** $`A = rR(\theta)`$ to compute $`\mathbf{v}' = A\mathbf{v}`$.


3. **Plot the new vector** $`\mathbf{v}'`$ in the same coordinate system.


This shows how the original vector is **rotated** by $`\theta`$ and **stretched/shrunk** by $r$.

**Example:**

Let $`\mathbf{v} = \begin{bmatrix} 1 \ 0 \end{bmatrix}`$ and

$`A = \begin{bmatrix} \cos 60^\circ & -\sin 60^\circ \\\sin 60^\circ & \cos 60^\circ \end{bmatrix} = \begin{bmatrix} \frac{1}{2} & -\frac{\sqrt{3}}{2} \\\frac{\sqrt{3}}{2} & \frac{1}{2} \end{bmatrix}`$

Then,

$`A \mathbf{v} = \begin{bmatrix} \frac{1}{2} \\\frac{\sqrt{3}}{2} \end{bmatrix} \Rightarrow \text{vector rotated by } 60^\circ`$

If $A$ is multiplied by $2$, it becomes a rotation-scaling matrix scaling the length by 2.

---

### **Summary Table**

| Concept                           | Description                                                   |
| --------------------------------- | ------------------------------------------------------------- |
| Rotation-Scaling Matrix           | $`A = r R(\theta)`$ combines uniform scaling and rotation     |
| Identify Rotation-Scaling         | Check if $`A = r R(\theta)`$ or has same form                 |
| Construct Rotation-Scaling Matrix | Multiply scaling factor $`r`$ by rotation matrix $`R(\theta)`$ |
| Find Scale and Angle              | Use $`r = \|A\mathbf{e}\_1\|`$ and match $`A/r`$ to $`R(\theta)`$ |
| Vector Transformation Sketch      | Plot original $`\mathbf{v}`$ and transformed $`A\mathbf{v}`$   |

