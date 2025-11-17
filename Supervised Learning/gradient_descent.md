# 🌟 **Gradient Descent for Linear Regression**

Gradient Descent is an **optimization algorithm** used to find the **best parameters (θ’s)** that minimize the error of the linear regression model.

---

# ✅ **1. Hypothesis Function**

For multivariate linear regression:

$$[
h_\theta(x) = \theta_0 + \theta_1 x_1 + \theta_2 x_2 + ... + \theta_n x_n
]

In vector form:

[
h_\theta(x) = \theta^T x
]$$

---

# ✅ **2. Cost Function (Mean Squared Error)**

Gradient descent minimizes:

$$
J(\theta) = \frac{1}{2m} \sum_{i=1}^{m} (h_\theta(x^{(i)}) - y^{(i)})^2
$$

Where

* ( m ) = number of training examples
* $( h_\theta(x^{(i)}) )$ = prediction
* $( y^{(i)} )$ = actual value

---

# ✅ **3. Gradient Descent Update Rule**

We update each parameter θ until the cost becomes minimum:
$$
[
\theta_j := \theta_j - \alpha \frac{1}{m}\sum_{i=1}^{m}(h_\theta(x^{(i)}) - y^{(i)})x_j^{(i)}
]
$$

Where
$
* ( \alpha ) = learning rate
* ( j = 0, 1, 2, ..., n )

For θ₀ (bias term), ( x_0 = 1 )
$
---

# 🎯 **4. Steps in Gradient Descent**

1. Initialize all θ’s with zeros or small random numbers
2. Repeat until convergence:

   * Compute predictions
   * Compute gradients
   * Update θ values
3. Stop when change in cost becomes very small

---

# ⚡ **5. Learning Rate (α) Matters**

| α Value    | Result                    |
| ---------- | ------------------------- |
| Too small  | Slow convergence          |
| Too large  | Diverges (J(θ) increases) |
| Just right | Fast convergence          |

---

# 🧠 **6. Gradient Descent Types**

| Type                                  | Description                          |
| ------------------------------------- | ------------------------------------ |
| **Batch Gradient Descent**            | Uses all training samples per update |
| **Stochastic Gradient Descent (SGD)** | Updates using 1 example at a time    |
| **Mini-batch GD**                     | Uses small batches (most practical)  |

---

# 📌 Simple Example

Suppose the model is:

$$h_\theta(x) = \theta_0 + \theta_1 x$$


Gradient updates:

$$
\theta_0 := \theta_0 - \alpha \frac{1}{m}\sum(h_\theta(x^{(i)}) - y^{(i)})

\theta_1 := \theta_1 - \alpha \frac{1}{m}\sum(h_\theta(x^{(i)}) - y^{(i)}) x^{(i)}
$$

---
