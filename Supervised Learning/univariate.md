# ⭐ **1. LINEAR REGRESSION WITH ONE VARIABLE (UNIVARIATE REGRESSION)**

This is the **simplest** supervised learning algorithm.



# 💡 **What is Linear Regression?**

It predicts a **continuous numerical value** using a straight line.

Examples:

* Predict house price based on size
* Predict marks based on study hours
* Predict weight based on height

You have **one input x** and **one output y**.

---

# ⭐ **Hypothesis Function**

Linear regression fits a line:

$h_\theta(x) = \theta_0 + \theta_1 x$

* $(\theta_0)$ = intercept
* $(\theta_1)$ = slope
* x = input
* output = prediction

This line should best fit the training data.

---

# ⭐ **Cost Function — Mean Squared Error (MSE)**

This tells how “bad” the line is.

$J(\theta_0, \theta_1) = \frac{1}{2m} \sum_{i=1}^m (h_\theta(x^{(i)}) - y^{(i)})^2$

Why squared error?

✔ Punishes large errors more
✔ Smooth curve → easy to optimize
✔ Mathematical convenience

Why divided by 2?
→ Makes derivative simpler.

---

# ⭐ **Goal of Linear Regression**

Find parameters $(\theta_0, \theta_1)$ that **minimize** the cost function.

This is classic optimization.

---

# ⭐ **How to Minimize Cost?**

Two important methods:

✔ 1. Gradient Descent (iterative)

 ✔ 2. Normal Equation (direct matrix solution)


---

# ⭐ **Gradient Descent Intuition**

Imagine you are on a mountain in the dark.
You want to reach the valley (minimum cost).
You take small steps downhill.

The slope (derivative) tells you the direction.

---

# ⭐ **Derivative (Learning Rule)**

$\theta_j := \theta_j - \alpha \frac{1}{m}\sum (h_\theta(x^{(i)}) - y^{(i)}) x_j^{(i)}$

* α = learning rate
* Repeat until convergence

Too large α → diverges
Too small α → very slow

---

# ⭐ **Geometric Interpretation**

Linear regression tries to find the **best straight line** that minimizes total error distance.

---

# ⭐ **Assumptions of Linear Regression**


1️⃣ Linearity: relationship between x and y is linear
2️⃣ Independence: observations independent
3️⃣ Homoscedasticity: equal variance
4️⃣ Normal distribution of errors
5️⃣ No multicollinearity (for multiple regression)

For **one variable**, only linearity and independence matter.

---

# ⭐ In short:

**Linear regression with one variable is the simplest supervised learning algorithm used to predict a continuous output. It assumes a linear relationship between the input variable x and output y. The hypothesis function is a straight line defined as (h_\theta(x)=\theta_0+\theta_1x). The parameters (\theta_0) and (\theta_1) are learned by minimizing the cost function, which is Mean Squared Error (MSE). The MSE is given by:**


$$J(\theta_0, \theta_1)=\frac{1}{2m}\sum_{i=1}^m (h_\theta(x^{(i)}) - y^{(i)})^2$$

**To find the parameter values that minimize the cost, gradient descent is used. Gradient descent iteratively updates the parameters using the formula:**


$$\theta_j := \theta_j - \alpha \frac{1}{m}\sum (h_\theta(x^{(i)}) - y^{(i)})x_j^{(i)}$$


**This process continues until convergence. Linear regression is widely used due to its simplicity, interpretability, and efficiency.**


