# ⭐ **LINEAR REGRESSION WITH MULTIPLE VARIABLES**

(Also called **Multivariate Linear Regression**)



# 💡 **Why Multiple Variables?**

Real-world predictions depend on **many factors**, not just one.

Example: Predict house price
⬆ size (sqft)
⬆ number of rooms
⬇ age of house
⬆ area rating

So we need multiple features:

$x_1, x_2, x_3, \ldots, x_n$

---

# ⭐ **Hypothesis Function (Vector Form)**

$h_\theta(x)=\theta_0 + \theta_1 x_1 + \theta_2 x_2 + \cdots + \theta_n x_n$

In vector notation:

$h_\theta(x) = \theta^T x$

Where:

* θ = parameter vector
* x = feature vector
* θᵀx = dot product

---

# ⭐ **Example**

House price predicted by:

$h_\theta(x)=\theta_0 + \theta_1(\text{size}) + \theta_2(\text{rooms}) + \theta_3(\text{age})$


This is a **hyperplane**, not a line.

---

# ⭐ **Cost Function (Same as before)**


$J(\theta)=\frac{1}{2m}\sum_{i=1}^m (h_\theta(x^{(i)}) - y^{(i)})^2$


We want θ values that minimize this.

---

# ⭐ **Gradient Descent for Multiple Variables**

Very similar to univariate case, but repeated for each parameter.

### Update rule:

$\theta_j := \theta_j - \alpha \frac{1}{m} \sum_{i=1}^m \left( h_\theta(x^{(i)}) - y^{(i)} \right) x_j^{(i)}$

Where j = 0, 1, …, n

---

# ⭐ **Feature Scaling (VERY IMPORTANT)**

(Always comes in university exams)

### Why?

If one feature is huge (like sqft = 1800)
and another is small (rooms = 3),
gradient descent becomes **VERY slow**.

### Solution:

Normalize values to range [-1, 1] or [0, 1]

Two methods:

### ✔ Mean Normalization

$x := \frac{x - \mu}{s}$


### ✔ Min-Max Scaling

$x := \frac{x - \text{min}}{\text{max}-\text{min}}$


This makes gradient descent converge faster.

---

# ⭐ **Vectorized Gradient Descent (Fast Form)**

Used in ML implementations.

$\theta := \theta - \alpha \frac{1}{m} X^T (X\theta - y)$

Where:

* X = matrix of features
* y = outputs vector

This is efficient for large datasets.

---

# ⭐ **Normal Equation (Matrix Method)**

Another way to compute θ **without gradient descent**:

$\theta = (X^T X)^{-1} X^T y$

### When to use this?

✔ small datasets

✔ few features (< 10,000)

✔ want exact solution

### When NOT to use?

✘ Very large features → matrix inverse expensive

✘ Overfitting might occur

---

# ⭐ **Interpretation of θ values**

* θ₀ → baseline prediction
* θ₁ → change in y when x₁ increases by 1 unit
* θ₂ → change in y when x₂ increases by 1 unit

This is why regression is **interpretable**.

---

# ⭐ In short:

**Linear regression with multiple variables extends simple linear regression to handle more than one input feature. If a dataset contains n features, the hypothesis function becomes a linear combination of all features and is represented as:**

$h_\theta(x)=\theta_0 + \theta_1 x_1 + \cdots + \theta_n x_n$


**In vector form:**

$h_\theta(x)=\theta^T x$


**The parameters θ are learned by minimizing the Mean Squared Error (MSE) cost function:**

$J(\theta)=\frac{1}{2m}\sum_{i=1}^m (h_\theta(x^{(i)}) - y^{(i)})^2$


**Parameter optimization is usually done using gradient descent, where each θ value is updated as:**

$\theta_j := \theta_j - \alpha \frac{1}{m}\sum (h_\theta(x^{(i)}) - y^{(i)})x_j^{(i)}$

**For faster convergence, feature scaling techniques such as mean normalization and min-max scaling are applied. An alternative to gradient descent is the Normal Equation:**


$\theta = (X^T X)^{-1} X^T y$

**This method directly computes θ without iteration.**
