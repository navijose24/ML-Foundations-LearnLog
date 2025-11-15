### Cluster Analysis


**Cluster: A collection of data objects**
    ◼ similar (or related) to one another within the same group
    ◼ dissimilar (or unrelated) to the objects in other groups


**Cluster analysis**
    ◼ Finding similarities between data according to the characteristics found in the data and grouping similar data objects into clusters.
    ◼ Clustering or cluster analysis is the task of grouping a set of objectsin such a way that objects in the same group (called a cluster) are more similar (in some sense) to each other than to those in other groups (clusters).
| Measure                 | Formula / Idea                                           | Used When                                      |
|-------------------------|----------------------------------------------------------|-------------------------------------------------|
| **Euclidean Distance**  | `d(x,y) = sqrt( sum_i (x_i - y_i)^2 )`                  | For numeric, continuous data (e.g., K-Means).   |
| **Manhattan Distance**  | `d(x,y) = sum_i |x_i - y_i|`                           | For grid-like data or sparse features.         |
| **Minkowski Distance**  | `d(x,y) = ( sum_i |x_i - y_i|^p )^(1/p)`                | General form; p=1 -> Manhattan, p=2 -> Euclid. |
| **Cosine Similarity**   | `S(x,y) = (x · y) / (||x|| * ||y||)`                    | For text vectors — measures angle, not distance.|
| **Jaccard Similarity**  | `S(A,B) = |A ∩ B| / |A ∪ B|`                            | For binary/categorical or set data.            |
| **Correlation coeff.**  | `corr(x,y)` measures linear relationship between vectors| Used in pattern and document clustering.       |
