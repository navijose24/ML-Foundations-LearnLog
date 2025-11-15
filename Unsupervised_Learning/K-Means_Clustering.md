# ⭐ **K-Means Clustering **

K-Means is the **most popular unsupervised clustering algorithm** used to group data into **K clusters**.

---

# 1️⃣ **What is the goal of K-Means?**

To divide data into **K groups** such that:

* Points **inside a cluster** are **similar**
* Points **across clusters** are **different**

It minimizes:

### **Within-Cluster Sum of Squared Error (WCSS)**

$\sum (x_i - \mu_k)^2$

---

# 2️⃣ **How K-Means Works (Algorithm Steps)**

### **Step 1: Choose K**

Decide how many clusters you want.

### **Step 2: Initialize centroids**

Randomly pick K points as initial “centers”.

### **Step 3: Assignment Step**

Assign each data point → closest centroid using **Euclidean distance**.

$\text{cluster}(x) = \arg\min_k ; d(x, \mu_k)$

### **Step 4: Update Step**

Recompute each centroid by taking the **mean** of points in that cluster.

$\mu_k = \frac{1}{N_k}\sum_{\text{points in }k} x_i$

### **Step 5: Repeat until convergence**

Converges when:

* Centroids stop changing, or
* Assignments don’t change

---

# 3️⃣ **Intuition (Why it works)**

K-Means tries to put each point close to a “center”.
Centers keep moving until everything settles.

Think of it like:
**People grouping around different leaders, and the leaders shifting to the center of their group.**

---

# 4️⃣ **Advantages**

✔ Simple & fast

✔ Works well on large datasets

✔ Easy to interpret

✔ Always converges

---

# 5️⃣ **Disadvantages**

❌ Needs K in advance

❌ Sensitive to initial centroids

❌ Sensitive to outliers

❌ Only works for spherical / convex clusters

---

# 6️⃣ **When to use K-Means?**

Use when:

* Data is **numeric & continuous**
* Clusters are round-shaped
* Dataset is large (1000+ points)
* You want fast unsupervised grouping

---

# 7️⃣ **When NOT to use K-Means?**

Avoid when:

* Data contains outliers
* Clusters are not spherical
* Clusters have very different sizes

---

# 8️⃣ **Practical**

📌 Always scale data (StandardScaler).
📌 Try multiple K using the **Elbow Method**.
📌 Use **k-means++** for better initialization.
📌 Run multiple times and pick best inertia.

---

### In short:

> K-Means is a partitional, centroid-based clustering algorithm that partitions data into K clusters. It minimizes the Within-Cluster Sum of Squared Error (WCSS). 
The algorithm repeats two steps: 
    (1) Assignment — assign each point to the nearest centroid using Euclidean distance, and 
    (2) Update — recompute centroids as the mean of all points in the cluster. The process continues until convergence.
>
> Advantages: simple, fast, works well on large datasets.
> Disadvantages: requires K, sensitive to initial values and outliers.
>
> Used for unsupervised grouping of continuous numeric data.

---
