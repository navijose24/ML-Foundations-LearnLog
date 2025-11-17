
# ⭐ **NON-LINEAR SVM (Kernel SVM)**

    Non-linear SVM uses kernel functions to map data into a higher-dimensional feature space where the data becomes linearly separable. The kernel trick avoids explicit computation of this mapping and allows SVM to learn non-linear decision boundaries. Common kernels include polynomial kernel and RBF kernel.


## **1️⃣ Problem with linear SVM**

A **linear SVM** can only separate data if the classes are divided by a straight line (linear boundary).

But many real-world datasets look like this:

⭕→🟡
🟡→⭕
(or circular patterns, spirals, XOR pattern)

These **cannot be separated by a straight line**.

So linear SVM fails.

---

# **2️⃣ Idea behind Non-Linear SVM**

Instead of trying to separate data **in the original 2D/3D space**,
we **map** the data into a **higher-dimensional space** where it *becomes linearly separable*.

### Example (very important for exam):

Imagine two circular classes:

* Inner circle = Class 0
* Outer ring = Class 1

No straight line can separate them.

But if we transform data like:

$z = x^2 + y^2$

Suddenly it becomes separable with a linear hyperplane in 3D.

---

# **3️⃣ Kernel Trick — Heart of Non-Linear SVM**

Mapping data to high dimensions is computationally expensive.

So SVM uses a shortcut called the **Kernel Trick**.

### ✔ Instead of computing:

$\phi(x)$

We directly compute the similarity using a kernel function:

$K(x_i, x_j) = \phi(x_i) \cdot \phi(x_j)$

This avoids actually “creating” the higher-dimensional space.

**SVM uses these kernels to form non-linear boundaries**.

---

# **4️⃣ Common Kernels**

## **1. Polynomial Kernel**

$K(x, y) = (x \cdot y + 1)^d$


* Adds polynomial features
* Degree **d** controls curvature
* Good for medium complexity boundaries

---

## **2. Radial Basis Function (RBF) Kernel**

(Most commonly used kernel)


$K(x, y) = \exp\left(-\gamma |x - y|^2\right)$


* Creates circular / curved decision boundaries
* Very powerful for general non-linear problems
* (\gamma) controls smoothness

**When data is messy → Use RBF**

---

## **3. Sigmoid Kernel**


$K(x, y) = \tanh(\alpha x \cdot y + c)$

* Behaves like a neural network activation
* Less used today

---

# **5️⃣ What Non-Linear SVM Actually Does**

It creates a **curved** decision boundary instead of a straight one.

Like this:

### Linear SVM:

```
-----------
```

### Non-linear SVM:

```
~~~~~~~ curved boundary ~~~~~~~
```

Because the kernel transforms the feature space.

---

**6️⃣ Simple example**

XOR Dataset:


* Top-left and bottom-right = Class 1
* Top-right and bottom-left = Class 0

No straight line works.
But with kernel SVM, the model can draw a curved boundary and separate them perfectly.

---

