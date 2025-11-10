### 🧠 Ensemble Methods


**Ensemble methods** combine the predictions of **multiple models** to create a **stronger, more accurate model** than any single one alone.
Idea → “Many weak learners together can make one strong learner.”

    > Ensemble learning improves model performance by combining multiple models to reduce bias, variance, or both. Bagging decreases variance, boosting reduces bias, and stacking learns optimal model combinations.

---

### 🎯 Why we use it:

* To **reduce overfitting** (variance).
* To **improve accuracy** and **stability**.
* To **handle complex patterns** that single models may miss.

---

### ⚙️ Main Types of Ensemble Methods:

| **Method**                          | **Concept**                                                                                                                                            | **Examples / Key Points**                                                                                             |
| ----------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------- |
| **Bagging (Bootstrap Aggregating)** | Trains multiple models (usually decision trees) on *different random subsets* of the data (using bootstrapping). Then averages or votes their results. | Example: **Random Forest** 🌳<br>✔️ Reduces variance<br>✔️ Good for unstable models like trees                        |
| **Boosting**                        | Trains models *sequentially*. Each new model focuses more on the errors of the previous one.                                                           | Examples: **AdaBoost**, **Gradient Boosting**, **XGBoost** 🚀<br>✔️ Reduces bias<br>✔️ Very powerful for tabular data |
| **Stacking**                        | Combines predictions of multiple different models (like SVM, Tree, Logistic Regression) using another “meta-model” to learn how to best mix them.      | ✔️ Flexible<br>✔️ Often gives top performance in competitions                                                         |

---

![advanced_ensemble_techniques](https://spotintelligence.com/wp-content/uploads/2024/03/bagging-boosting-stacking.jpg)

### 🧩 Example:

In Bagging → you train 10 decision trees on different bootstrap samples.
Each tree gives a prediction, and the final output is decided by **majority voting** (for classification) or **average** (for regression).


---