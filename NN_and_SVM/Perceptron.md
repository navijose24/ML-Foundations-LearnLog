## ⭐ **Perceptron**

    A perceptron is the simplest neural network — just ONE neuron.
    It takes inputs → multiplies by weights → adds bias → applies a function → gives output.

You can imagine it like a **decision maker**.

Example:
"Is the email spam?"
"Should I turn left or right?"

It makes **YES/NO** decisions (binary classification).

---

# 🧱 **Structure**

Inputs → Weights → Sum → Activation Function → Output

Example with 3 inputs:

```
x1 ------ w1
x2 ------ w2     → (w1*x1 + w2*x2 + w3*x3 + b) → activation → output
x3 ------ w3
```

---

# ⚙️ **Perceptron Formula**

**Weighted sum:**

$z = w_1x_1 + w_2x_2 + ... + w_nx_n + b$

**Activation function (Step function):**

$$
f(z) =
\begin{cases}
1 & \text{if } z \ge 0 \\
0 & \text{if } z < 0
\end{cases}
$$


**Final output:**

$y = f(z)$

---

# 🧠 **Intuition**

Think of the perceptron as a **judge**.

* Each input gives evidence (x)
* Each weight (w) tells how important that evidence is
* Bias (b) shifts the decision
* Step function decides **YES (1)** or **NO (0)**

If total evidence ≥ 0 → output is **1**

Else → output is **0**

---

🏋️ **Learning (Training) the Perceptron**

The perceptron learns by **adjusting weights** whenever it makes a mistake.

**Weight update rule**

$w_{new} = w_{old} + \eta (t - y)x$


**Bias update**


$b_{new} = b_{old} + \eta (t - y)$

Where

* t = true label
* y = predicted output
* $\eta$ = learning rate (0.01, 0.1 etc.)

---

# 🎯 Simple Example

Suppose you want the perceptron to learn **AND gate**:

| x1 | x2 | Output |
| -- | -- | ------ |
| 0  | 0  | 0      |
| 0  | 1  | 0      |
| 1  | 0  | 0      |
| 1  | 1  | 1      |

Start with random weights:
w1 = 0.2, w2 = –0.1, b = 0.0

For input (1,1):

$z = (1 × 0.2) + (1 × –0.1) + 0$
z = 0.1 → output = 1 (correct)

But for input (1,0):

$z = (1 × 0.2) + (0 × –0.1) + 0$
$0.2 ≥ 0 → output = 1 (WRONG — target is 0)$

So we update weights:

$w1 = w1 + η(t – y)x1$

$If η = 0.1:$

$w1 = 0.2 + 0.1(0 – 1)(1)$

$w1 = 0.2 – 0.1 = 0.1$

And so on…
Eventually the perceptron learns correct weights.

---

# Uses:

✔ Works only for **linearly separable** data

✔ Used for **binary classification**

✔ Uses **step activation**

✔ Learning is based on **perceptron rule**

✔ Cannot solve XOR

---

