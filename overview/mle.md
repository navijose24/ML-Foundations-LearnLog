# ⭐ **Maximum Likelihood Estimation (MLE)**



# 1️⃣ **What is MLE?**

MLE is a method to **find the parameter values** of a model that make the **observed data most probable**.

👉 We choose parameters θ that **maximize the likelihood** of seeing the given data.

---

# 2️⃣ **Why do we need MLE?**

Because machine learning models depend on parameters (θ).
MLE helps us **estimate the best values** of these parameters using data.

Examples:

* Mean & variance of a distribution
* Parameters in logistic regression
* Probabilities in Naive Bayes

---

# 3️⃣ **Likelihood Function**

If data = ( x_1, x_2, ..., x_n )
and model has parameter θ
then the **likelihood** is:

$L(\theta) = P(x_1, x_2, ..., x_n | \theta)$

If data points are **i.i.d**, then:

$L(\theta) = \prod_{i=1}^{n} P(x_i | \theta)$

---

# 4️⃣ **Log-Likelihood (Why we use it)**

Product becomes very small for large n → difficult to compute.
So we use **log** (monotonic):

$\ell(\theta) = \log L(\theta) = \sum_{i=1}^{n} \log P(x_i | \theta)$

---

# 5️⃣ **MLE Goal**

Find:

$\theta^{*} = \arg\max_{\theta} \ell(\theta)$

Often we:

* take derivative
* equate to zero
* solve for θ

---

# 6️⃣ **Example 1: MLE of Mean (Normal Distribution)**

Let data come from:

$$X \sim N(\mu, \sigma^2)$$

If σ² is known, MLE of μ is:

$$\mu_{MLE} = \frac{1}{n}\sum_{i=1}^{n} x_i$$

👉 The sample mean is the MLE.

---

# 7️⃣ **Example 2: MLE of Bernoulli (Coin toss)**

Data: 1, 0, 1, 1, 0
Parameter: p = P(heads)

Likelihood:

$$L(p) = p^{(\text{#heads})}(1-p)^{(\text{#tails})}$$

Log-likelihood:

$$\ell(p) = h \log p + t \log(1-p)$$

Differentiate and set = 0:

$$p_{MLE} = \frac{h}{h+t}$$

👉 **MLE = proportion of heads**.

---

# 8️⃣ **Properties of MLE**

1. **Consistent** — as n ↑, estimate → true value
2. **Efficient** — minimum variance
3. **Asymptotically normal**
4. **Invariant** — MLE of g(θ) = g(MLE of θ)

---

# 9️⃣ **Advantages**

* Works for many models
* Gives good estimates
* Easy with log-likelihood
* Has strong theoretical guarantees

---

# 🔟 **Disadvantages**

* Requires derivatives
* May give local maxima
* Sensitive to noise and outliers
* Requires assumptions (like i.i.d)

---

# 1️⃣1️⃣ In short:

### **Maximum Likelihood Estimation (MLE)**

MLE is a statistical method used to estimate the parameters of a model by maximizing the likelihood function. The likelihood represents the probability of the observed data given the model parameters. The goal of MLE is to find the parameter θ that makes the observed data most probable.

For independent and identically distributed (i.i.d.) data (x_1, x_2, …, x_n), the likelihood function is:

$L(\theta) = \prod_{i=1}^{n} P(x_i | \theta)$

Since the product becomes numerically unstable, the log-likelihood is used:

$\ell(\theta) = \sum_{i=1}^{n} \log P(x_i | \theta)$

The MLE estimate is obtained by maximizing the log-likelihood:

$\theta^{*} = \arg\max_{\theta} \ell(\theta)$

**Example:**
For a Bernoulli distribution, the MLE of probability (p) is:

$p_{MLE} = \frac{\text{number of successes}}{n}$

**Properties:**
MLE is consistent, efficient, asymptotically normal, and invariant.

MLE is widely used in regression, classification (logistic regression), and probabilistic models such as Naive Bayes.

---

