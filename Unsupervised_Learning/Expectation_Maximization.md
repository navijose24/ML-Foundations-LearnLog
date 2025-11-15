# ⭐ **Expectation–Maximization (EM) Algorithm**

*(Used for Soft Clustering / Probabilistic Clustering)*

---

# 1️⃣ What is EM? 

EM is an **iterative algorithm** used to estimate parameters of models when data has **hidden variables**.

In clustering, the hidden variable is:

👉 **Which cluster does each point belong to?**

Unlike K-Means (hard clustering), EM assigns:

👉 **Probability of belonging to each cluster**
(e.g., 0.7 to Cluster 1, 0.3 to Cluster 2)

This is why EM clustering = **soft clustering**.

---

# 2️⃣ Where is EM used?

Important applications:

✔ Gaussian Mixture Models (GMMs)

✔ Soft clustering

✔ Missing data problems

✔ Speech recognition

✔ Medical diagnosis

✔ Statistical estimation

---

# 3️⃣ Intuition (Why EM is needed)

You have **incomplete / hidden** information.

So EM alternates between:

* **Guessing the missing info** (E-Step)
* **Updating model based on the guess** (M-Step)

This loop continues until it stabilizes.

---

# 4️⃣ EM Algorithm Steps

EM has **two main steps** repeated until convergence:


🔵 **Step 1 — E-Step**

    Compute **responsibilities**:

    $r_{ik} = P(\text{cluster}=k \mid x_i)$

    This means:

    👉 For each point, calculate the **probability** of belonging to each cluster.

    We are *estimating the hidden data*.

    Example:
    Point ( $x_i$ ) belongs:

    * 0.8 probability → Cluster 1
    * 0.2 probability → Cluster 2

---

🔴 **Step 2 — M-Step (Maximization Step)**

    Using these probabilities, update:

    * Cluster means (centroids)
    * Cluster variances
    * Cluster weights

    $\mu_k = \frac{\sum r_{ik} x_i}{\sum r_{ik}}$

    $\sigma_k^2 = \frac{\sum r_{ik}(x_i - \mu_k)^2}{\sum r_{ik}}$

    $w_k = \frac{1}{N}\sum r_{ik}$

    This step **maximizes the likelihood** of the data given the updated parameters.

---

🌀 **Repeat E-Step and M-Step**

    Continue until:

    * Parameters do not change
    OR
    * Likelihood converges

---

# 5️⃣ Differences: **K-Means vs EM**

| Feature           | K-Means           | EM (GMM)                |
| ----------------- | ----------------- | ----------------------- |
| Type              | Hard clustering   | Soft clustering         |
| Assignments       | 0 or 1            | Probabilities           |
| Shape of clusters | Spherical         | Elliptical (flexible)   |
| Model             | Non-probabilistic | Probabilistic           |
| Output            | Centroids         | Mean, variance, weights |

👉 **EM is more powerful than K-Means**.

---

# 6️⃣ Advantages

✔ Soft clustering (more realistic)

✔ Handles overlapping clusters

✔ Handles complex shapes (Gaussian ellipses)

✔ Statistically sound

✔ Works even with missing data

---

# 7️⃣ Disadvantages

❌ Slow

❌ Can get stuck in local minima

❌ Sensitive to initialization

❌ Assumes data is Gaussian (in GMM version)

---

# 8️⃣ In short:

> **The EM algorithm is an iterative method used for soft clustering when data contains hidden variables. In clustering, EM estimates the probability that each point belongs to each cluster and updates parameters accordingly.
>
> The algorithm alternates between two steps.
> (1) E-Step: Compute the posterior probabilities (responsibilities) that each data point belongs to each cluster.
> (2) M-Step: Update the cluster parameters (mean, variance, and mixing weight) using these probabilities.
>
> This process is repeated until convergence. EM is widely used in Gaussian Mixture Models and soft clustering because it handles overlapping clusters and works well with incomplete data.**


---

