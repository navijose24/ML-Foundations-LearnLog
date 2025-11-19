# 🧩 Overview of Machine Learning

## 1. Machine Learning Paradigms

**1.1 Supervised Learning**

* **Definition:** Learning from labelled data (input + correct output).
* **Goal:** Learn a function ( f(x) \rightarrow y ).
* **Examples:** Classification (spam/ham), Regression (house price).
* **Algorithms:** Linear Regression, SVM, Decision Trees, Neural Networks.

**1.2 Unsupervised Learning**

* **Definition:** Learning patterns from **unlabelled data**.
* **Goal:** Discover hidden structure.
* **Examples:** Clustering (K-Means), Dimensionality Reduction (PCA).
* **Applications:** Customer segmentation, anomaly detection.

**1.3 Semi-Supervised Learning**

* **Definition:** Uses **few labelled + many unlabelled** samples.
* **Goal:** Improve accuracy when labels are expensive.
* **Examples:** Self-training, Graph-based methods.
* **Applications:** Text classification, medical imaging.

**1.4 Reinforcement Learning (RL)**

* **Definition:** Agent learns by interacting with an environment.
* **Key elements:** Agent, Environment, State, Action, Reward.
* **Goal:** Maximize cumulative reward.
* **Examples:** Q-learning, Deep Q Networks.
* **Applications:** Robotics, games, autonomous driving.

---

## 2. Basics of Parameter Estimation

Parameter estimation helps fit models to data.

**2.1 Maximum Likelihood Estimation (MLE)**

* **Goal:** Find parameters that **maximize the likelihood** of observed data.
* **Formula:** ( \theta_{MLE} = \arg\max_\theta P(D|\theta) )
* **Interpretation:** Choose parameters that make the data most probable.
* **Example:** Estimating mean of Gaussian.

**2.2 Maximum A Posteriori Estimation (MAP)**

* **Goal:** Incorporates **prior knowledge** using Bayes' theorem.
* **Formula:** ( \theta_{MAP} = \arg\max_\theta P(\theta|D) \propto P(D|\theta)P(\theta) )
* **Interpretation:** MLE + Prior.
* **Useful when:** Data is limited, need regularization.

---

### 3. Introduction to Bayesian Formulation

Bayesian modelling treats parameters as random variables.

**3.1 Bayes’ Theorem**

$$ 
P(\theta|D) = \frac{P(D|\theta)P(\theta)}{P(D)}
$$

**3.2 Components**

* **Prior (P(θ))**: What we believe *before* seeing data.
* **Likelihood (P(D|θ))**: How likely data is under a parameter.
* **Posterior (P(θ|D))**: Updated belief after seeing data.

**3.3 Why Bayesian?**

* Handles **uncertainty** better.
* Works well for small datasets.
* Allows updating beliefs with new data.

**3.4 Examples**

* Spam filtering (Bayesian classifier)
* Medical diagnosis (probabilistic reasoning)

---

