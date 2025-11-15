### Cluster Analysis


**Cluster: A collection of data objects**


    ◼ similar (or related) to one another within the same group
    ◼ dissimilar (or unrelated) to the objects in other groups


**Cluster analysis**


    ◼ Finding similarities between data according to the characteristics found in the data and grouping similar data objects into clusters.

    ◼ Clustering or cluster analysis is the task of grouping a set of objectsin such a way that objects in the same group (called a cluster) are more similar (in some sense) to each other than to those in other groups (clusters).


# ⭐ 1. Euclidean Distance

### **Definition:**
Straight-line distance between two points.

### **Formula (simple):**
$d(x,y) = \sqrt{\sum (x_i - y_i)^2}$

### **Use When:**
* Numeric, continuous data
* K-Means clustering
* Dense datasets

### **Intuition:**
Measures “how far” two points are.
*“Most commonly used distance. Sensitive to scale. Works best when features are normalized.”*

---

# ⭐ 2. Manhattan Distance (L1)

### **Definition:**
Distance by moving along right angles (like city blocks).

### **Formula:**
$d(x,y) = \sum |x_i - y_i|$

### **Use When:**
* Grid-like data
* Sparse data
* When outliers exist (more robust than Euclidean)

### **Intuition:**
Walking in a city → you move like a square path, not diagonally.
*“Less sensitive to outliers. Good for high-dimensional sparse data.”*

---

# ⭐ 3. Minkowski Distance

Generalization of Euclidean & Manhattan.

### **Formula:**
$d(x,y) = \left( \sum |x_i - y_i|^p \right)^{1/p}$

### **Special cases:**

* **p = 1 → Manhattan**
* **p = 2 → Euclidean**

### **Use When:**

You want to choose how strongly distance should react to differences.

### **Intuition:**

A customizable distance.
*“Minkowski = generalized Lp norm.”*

---

# ⭐ 4) Cosine Similarity

### **Definition:**
Angle between two vectors.

### **Formula:**
$\cos(\theta) = \frac{x \cdot y}{||x||,||y||}$

### **Use When:**
* Text data
* Document similarity
* High-dimensional vectors

### **Intuition:**
Doesn’t care about magnitude → only direction.

Example:
Two documents with same topic but different length should still be similar → cosine works best.

    *“Cosine similarity measures orientation, not distance. Good for sparse vectors.”*

---

# ⭐ 5) Jaccard Similarity

### **Definition:**
Similarity between sets.

### **Formula:**
$J(A, B) = \frac{|A \cap B|}{|A \cup B|}$

### **Use When:**
* Binary data
* Set comparison
* Text as sets of words

### **Intuition:**
Measures overlap divided by total unique items.

Example:
Similarity of two users’ liked movies.
    
    *“Used for categorical and binary attributes.”*

---

# ⭐ 6) Correlation Coefficient (Pearson)

### **Definition:**
Measures linear relationship between two variables.

### **Formula:**
$r = \frac{\text{cov}(x,y)}{\sigma_x \sigma_y}$

### **Use When:**
* You want to measure how variables change together
* Pattern recognition
* Document clustering

### **Intuition:**
+1 = move together
-1 = opposite
0 = unrelated

    *“Distance can be derived as 1 – correlation.”*

---

# COMPARISON 

| Measure         | Best For             | Type       |
| --------------- | -------------------- | ---------- |
| **Euclidean**   | Continuous data      | Distance   |
| **Manhattan**   | Sparse / grid        | Distance   |
| **Minkowski**   | Adjustable distance  | Distance   |
| **Cosine**      | Text vectors         | Similarity |
| **Jaccard**     | Binary / sets        | Similarity |
| **Correlation** | Linear relationships | Similarity |

---

