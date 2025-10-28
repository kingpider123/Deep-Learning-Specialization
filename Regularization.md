## 📘 Regularization Formulas

Regularization helps prevent overfitting by penalizing large weights in the model. Two common types are **L1** and **L2** regularization.

---

### 🔹 L2 Regularization (Ridge): 

Also known as **weight decay**, L2 regularization adds the squared magnitude of weights to the loss function.

**Formula:**



$$
J(w, b) = \frac{1}{m} \sum_{i=1}^{m} \mathcal{L}(\hat{y}^{(i)}, y^{(i)}) + \frac{\lambda}{2m} \sum_{j=1}^{n_x} w_j^2
$$



- $ \mathcal{L} $: original loss (e.g., cross-entropy)
- $ \lambda $: regularization parameter
- $ m $: number of training examples
- $ w_j $: weight parameters

---

### 🔸 L1 Regularization (Lasso)

L1 regularization adds the absolute value of weights to the loss function, encouraging sparsity.

**Formula:**



$$
J(w, b) = \frac{1}{m} \sum_{i=1}^{m} \mathcal{L}(\hat{y}^{(i)}, y^{(i)}) + \frac{\lambda}{m} \sum_{j=1}^{n_x} |w_j|
$$



- Promotes sparsity (many weights become exactly zero)
- Useful for feature selection

---

### 🧠 Notes

- L2 is more commonly used in deep learning.
- L1 is often used when model interpretability or feature selection is important.
- You can also combine both (Elastic Net).

# Dropout Regularization
When you iterate through each layer of a neural network, you toss a coin with a probability of eliminating a hidden unit in that layer.---> Can't rely on any one feature, so have to spread out weight ----> Shrinking the squared norm of the weight

This makes the neural network much smaller.