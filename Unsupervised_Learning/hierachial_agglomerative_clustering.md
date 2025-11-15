# ⭐ **Hierarchical Agglomerative Clustering (HAC)**



# 1️⃣ **What is Hierarchical Clustering?**

A clustering method that builds a **tree-like structure** (called a **dendrogram**) to represent how data points are grouped.

There are two types:

### **1. Agglomerative (bottom-up)** 

Start with each point as a cluster → keep merging.

### **2. Divisive (top-down)**

Start with one cluster → keep splitting.


---

# 2️⃣ **Agglomerative Clustering: Step-by-Step**



Start with **N clusters** (each point is its own cluster).

### **Step 1:** Compute distance matrix

Find pairwise distances between all points.

### **Step 2:** Find the closest two clusters

Pick the pair with minimum distance.

### **Step 3:** Merge them

Combine the two clusters into one.

### **Step 4:** Update the distance matrix

Update distances between new cluster vs others using **linkage methods**.

### **Step 5:** Repeat until only 1 cluster remains

This forms a **hierarchy of clusters**, visualized using a **dendrogram**.

---

# 3️⃣ **Linkage Methods **

These methods decide **how to measure distance between two clusters**.

### ✔ **1. Single Linkage**

Distance = minimum distance between any two points in the clusters.

$D(A,B) = \min_{i \in A, j \in B} d(i,j)$

**Effect:** Can form long, chain-like clusters (**chaining effect**).

---

### ✔ **2. Complete Linkage**

Distance = maximum distance between points.

$D(A,B) = \max_{i \in A, j \in B} d(i,j)$

**Effect:** Produces compact, tight clusters.

---

### ✔ **3. Average Linkage**

Distance = average distance between all pairs.

$D(A,B) = \text{avg}_{i \in A, j \in B} d(i,j)$

**Effect:** Balanced clusters (between single & complete).

---

### ✔ **4. Ward’s Method**

Merges clusters that result in the **smallest increase in WCSS**.

**Effect:** Works well for numeric data (very popular).

---

# 4️⃣ **Advantages**

✔ No need to choose K in advance

✔ Produces dendrogram (full hierarchy)

✔ Works for any shape clusters

✔ Good for small datasets

---

# 5️⃣ **Disadvantages**

❌ Computationally expensive (O(n²))

❌ Cannot undo merges (greedy algorithm)

❌ Sensitive to noise & outliers

❌ Hard for very large datasets

---

# 6️⃣ **When to Use HAC?**

Use when:

* You want a **visual hierarchy** (dendrogram).
* Dataset is **small/medium**.
* You don’t know how many clusters to choose.
* You need explainability.

---

# 7️⃣ **Dendrogram**

A tree diagram showing how clusters are merged.

Use it to:

* Choose number of clusters
* Understand cluster relationships

You “cut” the dendrogram horizontally to get K clusters.

---

# 📌 In short:

> **Hierarchical agglomerative clustering is a bottom-up clustering technique where each data point starts as its own cluster, and the algorithm repeatedly merges the closest pair of clusters based on a similarity measure. The process is repeated until all points belong to a single cluster, forming a hierarchical structure called a dendrogram.
>
> The distance between clusters can be defined using linkage methods: Single linkage (minimum distance), Complete linkage (maximum distance), Average linkage (mean distance), and Ward’s method (minimizes increase in within-cluster variance).
>
> Advantages: no need to choose K, produces dendrogram, works for different cluster shapes.
> Disadvantages: high computational cost, irreversible merges, sensitive to noise.**



---
