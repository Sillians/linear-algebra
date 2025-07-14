# **Finding a Basis of a Span – Deep Dive**

A **basis** of a span is a minimal set of **linearly independent vectors** that still **span the same space** as the original set. 
It gives the most compact and efficient description of that space.

---

## **1. Definitions**

* **Span**: The set of all linear combinations of a set of vectors.
* **Basis**: A linearly independent set of vectors that spans the space.
* **Dimension**: The number of vectors in the basis.

---

## **2. Finding a Basis by Inspection**

When vectors are obviously linearly dependent or contain multiples of each other, you can identify a basis quickly.

### **Example**

Given:

```
v₁ = [1, 2]
v₂ = [2, 4]
v₃ = [3, 0]
```

* Notice: `v₂ = 2 * v₁` → linearly dependent.
* `v₁` and `v₃` are not multiples → linearly independent.

### Basis:

```
{
  [1, 2],
  [3, 0]
}
```

---

## **3. Finding a Basis by Identifying Pivot Columns**

If inspection isn't obvious, use **row reduction** to identify **pivot columns** of the matrix formed by placing vectors as columns.

### **Steps**

1. Form a matrix with the vectors as columns.
2. Perform row reduction (RREF).
3. Columns in the original matrix corresponding to pivot columns in RREF form a basis.

### **Example**

Given:

```
A =
[1  2  3
 2  4  6
 0  1  1]
```

Row reduce A:

```
RREF(A) =
[1  2  3
 0  0  0
 0  1  1]
```

* Pivot columns: Columns 1 and 3 in RREF → Correspond to columns 1 and 2 in the original matrix.

###  Basis:

```
{
  [1, 2, 0],
  [2, 4, 1]
}
```

---

## **4. Determining Whether a Given Set Is a Basis**

To determine if a set is a basis, check:

* **Linear Independence**: No vector in the set can be written as a linear combination of the others.
* **Spanning**: The set can be used to produce all vectors in the space.

### **Example**

Given:

```
v₁ = [1, 0, 0]
v₂ = [0, 1, 0]
v₃ = [1, 1, 0]
```

Check if vectors are linearly independent:

```
v₃ = v₁ + v₂ → dependent
```

So, the set `{v₁, v₂, v₃}` is **not** a basis.

### Valid Basis:

```
{
  [1, 0, 0],
  [0, 1, 0]
}
```

---

## **Summary Table**

| Method              | When to Use            | Tools                   |
| ------------------- | ---------------------- | ----------------------- |
| **Inspection**      | Simple dependencies    | Scalar multiples        |
| **Pivot Columns**   | Complex/many vectors   | Gaussian elimination    |
| **Check Given Set** | Validating a candidate | Independence + Spanning |
