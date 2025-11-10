## 🧠 What is Unsupervised Learning?


> Unsupervised learning finds patterns or clusters from unlabeled data by analyzing similarities or relationships among input features.


* **Definition:**
  Unsupervised learning deals with **unlabeled data** — the model tries to find *hidden patterns or structures* in data **without predefined output labels**.

* **Goal:**
  Discover groups, similarities, or underlying dimensions in data.

---

### 📘 Common Tasks:

| **Task**                     | **Purpose**                                       | **Examples**                             |
| ---------------------------- | ------------------------------------------------- | ---------------------------------------- |
| **Clustering**               | Group similar data points together                | Customer segmentation, document grouping |
| **Dimensionality Reduction** | Reduce data features while keeping important info | PCA, t-SNE, Autoencoders                 |

---

### 🧩 Difference from Supervised Learning:

| **Aspect**     | **Supervised Learning**          | **Unsupervised Learning**                 |
| -------------- | -------------------------------- | ----------------------------------------- |
| **Data Type**  | Labeled data (has target/output) | Unlabeled data                            |
| **Goal**       | Predict outcome (Y)              | Find structure/patterns                   |
| **Examples**   | Regression, Classification       | Clustering, PCA                           |
| **Evaluation** | Accuracy, Precision, Recall      | Silhouette score, Within-cluster distance |

---

### 📊 Example:

You have a dataset of 1000 customers — no info on their “type.”
Unsupervised algorithms like **K-Means** can automatically find clusters such as:

* Cluster 1: Budget buyers 🛍️
* Cluster 2: Luxury buyers 💎
* Cluster 3: Occasional shoppers 🕒

---
