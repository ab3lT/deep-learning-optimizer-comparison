# deep-learning-optimizer-comparison

A comparative study of deep learning optimization algorithms using a simple neural network. Evaluates Gradient Descent variants and adaptive optimizers on classification performance using accuracy and F1 score.

- **Choose an appropriate problem** and solve it using Deep Learning (use a simple network).
- **Use visualization tools** as much as possible.
- **Presentation is required.**

### Evaluation Metrics

- **Accuracy**
- **F1 Score**

### Objective

Compare the performance of the optimization algorithms in solving the selected problem.

### Experimental Setup

- The experimental setup should be **identical for each group of algorithms**.

### Comparisons to Make

1. **Part-I algorithms**
2. **Part-II algorithms**
3. **Part-III algorithms**
4. **The best algorithm from each group**

Finally, **rank all 7 algorithms** based on their performance.

---

### Expected Deliverables

- **Running, error-free code** with sufficient visualization and important output screens.
- **Report** sufficiently describing your implementation (could be a slide or a PDF).
- **Do not zip the files**; submit them as they are.

---

### Algorithm Groups

#### Part-I

1. Gradient Descent (GD/Batch GD)
2. Minibatch SGD
3. Stochastic Gradient Descent

#### Part-II

4. Gradient Descent
5. Gradient Descent with Momentum
6. Gradient Descent with Nesterov Momentum

#### Part-III

7. AdaGrad
8. RMSProp
9. Adam

# Final Algorithm Performance Summary

## Part I: Batch vs. Stochastic Methods

| Algorithm       | Accuracy | F1 Score  | Key Insight                          |
|-----------------|----------|-----------|--------------------------------------|
| **Stochastic GD** | 0.8664   | 0.8661    | Frequent updates prevent stagnation  |
| MiniBatch SGD    | 0.8366   | 0.8362    | Balanced batch updates               |
| Batch GD         | 0.2043   | 0.1676    | Failed to converge                   |

**Best**: **Stochastic GD**  
*Why?* Single-sample updates enabled escape from poor local minima that trapped Batch GD.

---

## Part II: SGD Variants

| Algorithm         | Accuracy | F1 Score  | Key Insight                          |
|-------------------|----------|-----------|--------------------------------------|
| **SGD + Nesterov** | 0.8746   | 0.8738    | Look-ahead gradient calculation      |
| SGD + Momentum    | 0.8715   | 0.8718    | Momentum dampens oscillations        |
| Vanilla SGD       | 0.8471   | 0.8472    | Baseline performance                 |

**Best**: **SGD + Nesterov**  
*Why?* Predictive parameter position evaluation yielded smoother convergence than standard momentum.

---

## Part III: Adaptive Optimizers

| Algorithm | Accuracy | F1 Score  | Key Insight                          |
|-----------|----------|-----------|--------------------------------------|
| **Adam**   | 0.8809   | 0.8788    | Momentum + adaptive learning rates   |
| RMSprop    | 0.8773   | 0.8770    | Gradient magnitude normalization     |
| Adagrad    | 0.8138   | 0.8088    | Aggressive rate decay                |

**Best**: **Adam**  
*Why?* Hybrid approach combined the benefits of momentum and per-parameter adaptation.

---

## Cross-Part Comparison

| Category          | Best Algorithm | Accuracy | Advantage Over Runner-Up |
|--------------------|----------------|----------|---------------------------|
| Basic Optimization | Stochastic GD  | 0.8664   | +2.98% over MiniBatch SGD |
| Momentum Variants  | SGD + Nesterov | 0.8746   | +0.31% over SGD+Momentum  |
| Adaptive Methods   | Adam           | 0.8809   | +0.36% over RMSprop       |

**Overall Champion**: **Adam** (0.8809 accuracy)  
Demonstrates the power of combining momentum with adaptive learning rates in deep learning optimization.
