# ⭐ **ACTIVATION FUNCTIONS**


# 💡 **What is an Activation Function?**

An activation function decides whether a neuron should “fire” or not.

It introduces **non-linearity** → this allows neural networks to learn **complex patterns**.

Without activation functions → your network becomes a simple linear model → totally useless for real-world problems.

---

# 🧠 **Why We Need Activation Functions?**

Because real-world data is **non-linear**:

* Images
* Speech
* Emotions
* Natural language
* Business patterns

Activation functions create **curves and bends** so the network can learn the real patterns.

---

# ⭐ TYPES OF ACTIVATION FUNCTIONS


# 1️⃣ **Sigmoid Function (Logistic)**

**Formula:**

$f(x) = \frac{1}{1 + e^{-x}}$

**Range:** 0 to 1
**Shape:** S-shaped curve

![Sigmoid Function](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQovfM4UAyi_a07pWKNPQpX8_JFU5851Gk_VO8bMpWptb6GIh9YMlMhecNIFUNf3TbAVezNUuF_)

### **Where to use:**

✔ Binary classification output layer

✔ Probabilities (0–1)

### **Advantages:**

* Smooth curve
* Output is probability-like

### **Disadvantages:**

* Vanishing gradient problem
* Saturates at extreme ends
* Slow learning

---

# 2️⃣ **Tanh (Hyperbolic Tangent)**

**Formula:**

$f(x) = \tanh(x)$

**Range:** –1 to +1


![Tanh (Hyperbolic Tangent)](https://miro.medium.com/v2/resize:fit:756/1*tOc--h-QU9_bHqWLPY9YLA.png)


### **Where to use:**

✔ Hidden layers (better than sigmoid)

### **Advantages:**

* Zero-centered output
* Stronger gradient than sigmoid

### **Disadvantages:**

* Still has vanishing gradient

---

# 3️⃣ **ReLU (Rectified Linear Unit)**

**Formula:**

$f(x) = \max(0, x)$

![ReLu](https://cdn.prod.website-files.com/614c82ed388d53640613982e/64a6c16cff99b6337d9dacf7_parametric%20relu%20and%20first%20derivative.webp)

### **Where to use:**

✔ All modern deep neural networks

✔ CNNs, RNNs, Transformers

### **Advantages:**

* No vanishing gradient for x > 0
* Simple and fast
* Best for hidden layers

### **Disadvantages:**

* Dead ReLU problem (neurons stop updating if x < 0 always)

---

# 4️⃣ **Leaky ReLU**

Fixes ReLU’s “dead neuron” problem.

**Formula:**
$$
f(x) =
\begin{cases}
x & x > 0 \
0.01x & x \le 0
\end{cases}
$$


![leaky ReLu](https://cdn.analyticsvidhya.com/wp-content/uploads/2017/10/prelu-300x262.png)

### **Where to use:**

✔ When ReLU neurons die

✔ Deep networks

---

# 5️⃣ **Softmax**

Used only in **multi-class classification (output layer)**.

**Formula:**

$\sigma(z_i)=\frac{e^{z_i}}{\sum_{j=1}^{K} e^{z_j}}$

![soft max](images/softmax.png)

### **Where to use:**

✔ Multi-class output (cat, dog, horse)

✔ Probability distribution (sums to 1)

---

# 📌 In short:

| Activation     | Range   | Use Case           | Pros                 | Cons                  |
| -------------- | ------- | ------------------ | -------------------- | --------------------- |
| **Sigmoid**    | 0 to 1  | Binary output      | Probability          | Vanishing gradient    |
| **Tanh**       | –1 to 1 | Hidden layers      | Zero-centered        | Can still saturate    |
| **ReLU**       | 0 to ∞  | Hidden layers      | Fast, no VG          | Dead neurons          |
| **Leaky ReLU** | –∞ to ∞ | Deep hidden layers | Fixes dead ReLU      | Slight noise          |
| **Softmax**    | 0–1     | Multi-class output | Best for multi-class | Expensive computation |

---

# ⭐ Why Activation Functions Matter for Backpropagation?

Because backpropagation uses **derivatives**.
Activation functions must be:

* Differentiable
* Smooth
* Non-linear

ReLU, Sigmoid, Tanh → all have derivatives → so backprop can update weights.

---