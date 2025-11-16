# ⭐ **BACKPROPAGATION ALGORITHM**

(The heart of training neural networks)

💡 **What is Backpropagation?**

Backpropagation = **how a neural network learns** by correcting its mistakes.

It is a **learning algorithm** used to update weights using:

1. **Forward pass** → make prediction
2. **Find error** (difference between predicted & actual)
3. **Backward pass** → send error back through the network
4. **Update weights** using gradient descent

It is basically:
👉 “I predicted wrong → let me adjust my weights → try again”

---


⚙️ **WHY do we need backprop?**

Because in multilayer networks (many hidden layers), we can’t manually find how much *each* weight contributed to the error.

Backprop tells us:
“How responsible was each weight for the final error?”

Then it updates that weight accordingly.

---


🧱 **STEPS OF BACKPROPAGATION**

Full pipeline clearly.

---


✔ **STEP 1: Forward Propagation**

Input → Hidden layer → Output
Compute:

$z = w_ix_i + b$

$a = f(z)$

You get a prediction ŷ.

---


✔ **STEP 2: Compute Error (Loss)**

Most common loss:


**Mean Squared Error (MSE)**

$E = \frac{1}{2}(t - y)^2$

Where
t = true output
y = predicted output

---


✔ **STEP 3: Backward Propagation (Chain Rule)**

You compute how much **each weight** contributed to the error.

This is done using **partial derivatives**:

$\frac{\partial E}{\partial w}$

This derivative tells us:
“If I change the weight w by a little, how much will the error change?”

---

## ✔ **STEP 4: Weight Update Rule**

Using **Gradient Descent**:

$w_{new} = w_{old} - \eta \frac{\partial E}{\partial w}$

Where
$η (eta)$ = learning rate

This reduces the error.

---

# 🧠 **INTUITIVE**

Imagine you are throwing a dart and miss the target.

Forward pass → You throw the dart
Loss → The distance from the center
Backward pass → Someone tells you “move your hand slightly left”
Weight update → You adjust your position
Repeat → Throw until you hit the center

Same idea in neural networks.

---

# ⭐ EXAMPLE 

Consider 1 neuron with sigmoid activation.

**Forward pass:**

1. Compute weighted sum z
2. Apply sigmoid
3. Get prediction y


**Backward pass:**

Compute:

1. Derivative of loss wrt output
2. Derivative wrt activation
3. Derivative wrt weight

Finally update weight.

---

🎯 **Why Chain Rule?**

Because in multi-layer networks:

Input → Hidden → Hidden → Output

Each layer affects the next.
Chain rule tells how error flows **layer-by-layer backwards**.

---

# 🎓 In short:


“Backpropagation is a supervised learning algorithm used to train multilayer neural networks by propagating the error backward and updating the weights using gradient descent.”

**Key Steps:**

1. **Forward pass** – compute output
2. **Compute error**
3. **Backward pass** – compute gradients using chain rule
4. **Update weights** using gradient descent

 **Advantages:**

✔ Efficient for deep networks

✔ Computes exact gradients

✔ Allows training multi-layer networks

✔ Works with any differentiable activation function

**Disadvantages:**

✘ Requires differentiable functions

✘ Suffers from vanishing gradients (sigmoid/tanh)

✘ Slow if too many layers

✘ Sensitive to learning rate

**Applications:**

* Deep learning
* Image classification
* Speech recognition
* Time-series forecasting
* Medical diagnosis
* NLP (transformers, RNNs, etc.)

---