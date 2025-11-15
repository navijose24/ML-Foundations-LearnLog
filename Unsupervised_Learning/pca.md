# ⭐ **Principal Component Analysis (PCA)**

Dimensionality Reduction → Unsupervised Learning

---

# 1️⃣ **What is PCA?**

PCA is a mathematical technique that:

👉 **Reduces the number of features**
👉 **Keeps maximum possible information**
👉 **Transforms data into new axes called Principal Components**

These new axes capture the most variance in the data.

---

# 2️⃣ **Why do we use PCA?**


✔ Remove redundant or correlated features

✔ Reduce noise

✔ Visualize high-dimensional data

✔ Speed up ML algorithms

✔ Prevent overfitting

✔ Makes clustering/ML more stable

---

# 3️⃣ **Intuition**

Imagine a dataset that lies along a **diagonal line**.
But your axes (x, y) are horizontal and vertical — not aligned with the data.

PCA **rotates** the axes:

* PC1 → direction of maximum spread
* PC2 → direction of remaining spread

So PCA finds **best directions** to represent your data.

---

# 4️⃣ **How PCA Works — Step By Step**

**Step 1: Standardize the data**

Mean = 0, variance = 1
Why?
Because PCA is affected by scale.

**Step 2: Compute the Covariance Matrix**
$C = \frac{1}{n-1}X^TX$

This matrix shows how features vary together.

**Step 3: Compute Eigenvalues & Eigenvectors of Covariance Matrix**

* **Eigenvalues** → importance (variance explained)
* **Eigenvectors** → directions (principal components)

**Step 4: Sort Eigenvalues in descending order**

PC1 = highest eigenvalue
PC2 = second highest
PCk = kth eigenvalue

Higher eigenvalue = more variance.

**Step 5: Select top K components**

Choose K such that the cumulative variance is enough (e.g., 95%).

**Step 6: Transform data onto the new subspace**

$Y = X \cdot W$

Where W = matrix of selected eigenvectors.

This gives us **reduced-dimensional data**.

---

# 5️⃣ **Variance **

The proportion of variance captured by each component:

$\text{Explained variance} = \frac{\lambda_i}{\sum \lambda}$

Used to choose number of components.

---

# 6️⃣ **Advantages**

✔ Reduces dimensionality efficiently

✔ Removes noise

✔ Makes algorithms faster

✔ Handles correlated features

✔ Helps visualization (2D, 3D)

---

# 7️⃣ **Disadvantages**

❌ Components lose original meaning

❌ Linear method → can’t catch non-linearity

❌ Sensitive to scaling

❌ Sensitive to outliers

---

# 8️⃣ **Where PCA is used?**

✔ Image compression

✔ Face recognition

✔ Data visualization

✔ Noise reduction

✔ Preprocessing before clustering/classification

---

# 9️⃣ In short:

> **PCA is a dimensionality reduction technique that transforms data into a new coordinate system such that the greatest variance lies on the first principal component, the second greatest on the second component, and so on.
>
> Steps: (1) Standardize the data. (2) Compute the covariance matrix. (3) Calculate eigenvalues and eigenvectors. (4) Sort eigenvalues in descending order. (5) Select top K eigenvectors. (6) Transform the original data onto the new reduced space.
>
> PCA reduces redundancy, increases efficiency, and is widely used for visualization, noise reduction, and preprocessing before clustering.**



---