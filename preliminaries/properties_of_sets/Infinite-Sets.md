## **Infinite Sets**

---

### **1. Understanding Infinite Sets**

An **infinite set** is a set that contains an unending number of elements. Unlike finite sets, infinite sets cannot be counted to completion.

Infinite sets can be **countably infinite** (can be put in one-to-one correspondence with the natural numbers, 
like $`\mathbb{Z}, \mathbb{Q}`$) or **uncountably infinite** (like $`\mathbb{R}`$).

---

### **2. Sets Defined Using Inequalities**

Sets defined with inequalities often produce infinite sets. For example:

* $`A = \{ x \in \mathbb{R} : x > 3 \}`$
  → Contains all real numbers greater than 3 — **uncountably infinite**.


* $`B = \{ n \in \mathbb{Z} : n \leq -5 \}`$
  → Contains all integers less than or equal to −5 — **countably infinite**.


* $`C = \{ x \in \mathbb{N} : x^2 < 1000 \}`$
  → This is **finite**, since it’s bounded.
  Contrast: $`D = \{ x \in \mathbb{N} : x^2 > 1 \}`$ → **infinite**.

---

### **3. Sets Defined Using Trigonometric Equations**

Trigonometric functions are periodic, so sets defined using these often yield **infinite sets**.

* $`A = \{ x \in \mathbb{R} : \sin x = 0 \}`$
  → Solutions: $`x = n\pi`$, for $`n \in \mathbb{Z}`$ — **countably infinite**.


* $`B = \{ x \in \mathbb{R} : \tan x = 1 \}`$
  → Solutions: $`x = \frac{\pi}{4} + n\pi`$, for $`n \in \mathbb{Z}`$ — **countably infinite**.


* $`C = \{ x \in \mathbb{Q} : \cos x = 0 \}`$
  → This set is **finite or possibly empty**, since cosine only equals 0 at irrational multiples of $`\pi`$.

---

### **4. Sets Defined Using Derivatives**

A derivative-based condition can also define an infinite set.

* $`A = \{ x \in \mathbb{R} : f'(x) = 0 \}`$
  If $`f`$ is a constant function, then this is **all of $`\mathbb{R}`$** — **uncountably infinite**.


* $`B = \{ x \in \mathbb{R} : \frac{d}{dx} \sin x = 0 \}`$
  That is, $`\cos x = 0`$ → $`x = \frac{\pi}{2} + n\pi`$, $`n \in \mathbb{Z}`$ — **countably infinite**.


* $`C = \{ x \in \mathbb{Z} : \frac{d}{dx} x^2 = 0 \}`$
  → No such $`x \in \mathbb{Z}`$, so **empty set**.

---

### ✅ Summary

| Definition Type                  | Example Set                            | Infinite? | Type        |
| -------------------------------- | -------------------------------------- | --------- | ----------- |
| Inequality                       | $`\{ x \in \mathbb{R} : x > 0 \}`$       | Yes       | Uncountable |
| Trigonometric Equation           | $`\{ x \in \mathbb{R} : \sin x = 0 \}`$  | Yes       | Countable   |
| Derivative-Based                 | $`\{ x : f'(x) = 0 \}$ for constant $f`$ | Yes       | Uncountable |
| Derivative-Based + Trig Function | $`\{ x : \cos x = 0 \}`$                 | Yes       | Countable   |

Infinite sets appear in diverse contexts and require careful attention to domain (ℝ, ℤ, ℚ) and function behavior.
