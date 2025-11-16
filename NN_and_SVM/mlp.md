#  **MULTILAYER FEED-FORWARD NETWORK (MLP / ANN)**


# 💡 What is it?

A **Multilayer Feed-Forward Neural Network (MLP)** is a neural network with:

* **Input layer**
* **One or more hidden layers**
* **Output layer**

Each layer passes information **forward only** → no loops.

It looks like this:

```
Input → Hidden Layer 1 → Hidden Layer 2 → Output
```

This is how **modern neural networks** like image classifiers, speech recognition, ChatGPT's base ideas, etc., work.

---

# 🧱 Structure of MLP

### 🟦 **1. Input layer**

Receives the raw data
Example: 28×28 pixels → 784 inputs

---

### 🟪 **2. Hidden layers**

* Perform transformations
* Extract patterns
* Contain neurons with activation functions

Example:

```
100 neurons → extract features
50 neurons → extract deeper features
```

---

### 🟥 **3. Output layer**

For:

* Binary classification → 1 neuron (sigmoid)
* Multi-class → n neurons (softmax)
* Regression → 1 neuron (linear)

---

# ⚙️ **Math Behind One Neuron**

Each neuron does this:

### 1. Weighted sum:

$z = \Sigma(w_ix_i) + b$

### 2. Activation function:

$a = f(z)$

Activation function gives **non-linearity**.

---

# ⚡ Why "Feed-Forward"?

Because information *flows only forward*, like:

Input → Hidden → Output
No feedback loops.

This prevents infinite loops.

---

# 🧠 What Problems Can MLP Solve?

✔ Non-linear problems
✔ XOR problem (perceptron cannot do this)
✔ Classification
✔ Regression
✔ Pattern recognition

---

# 🌟 Difference from Perceptron

| Perceptron         | MLP                      |
| ------------------ | ------------------------ |
| Only 1 layer       | Many layers              |
| Solves only linear | Solves non-linear        |
| Uses step function | Uses sigmoid, ReLU, tanh |
| Cannot solve XOR   | Can solve XOR            |

---

# 🎯 Why MLP Works Better?

Because of **Hidden Layers + Activation Functions**.

Hidden layers extract features:

* edges
* patterns
* shapes
* correlations

More layers = deeper understanding.

---

# 📌 In short:

1. MLP consists of **input, hidden, and output layers**
2. Neurons perform **weighted sum + activation function**
3. Information flows **forward only**
4. Trained using **Backpropagation algorithm**
5. Can model **non-linear decision boundaries**
6. Can solve problems like **XOR**
7. Uses **ReLU, Sigmoid, Tanh** etc.

---

