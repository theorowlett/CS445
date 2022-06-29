### AI/ML Overview
---
#### What is Machine Learning?
- Detecting patterns and regularities with a good and generizable approximation ("model" or "hypothesis")
- Could be supervised as unsupervised
- Supervised
  - Data that contains labels, ground truth labels
  - Can we predict new labels?
- Unsupervised
  - Extract general patterns in the absense of labels
  - clustering
- There's also reinforcement learning, we're not going in depth on it.

---
#### Supervised learning
- Goal is to learn a mapping from **inputs** (X) to **labels** (Y)
  - $$ f: X \to Y $$
- Commonly X denotes the **design matrix**, where X is of dimensions $n*d$.
- **Regression**: When $y \in \mathbb{R}$ (**the label is a real-value**)
  - Eg. Predict expected income from education level.
  - 
- **Classification**: When $y \in {1,...,K}$ (**the label is categorical**)
  - Eg. Predict which image contains a pedestrian.
  - Decision boundary seperates classes
---
#### Mapping
- General goal in ML is to learn the true mapping $f$
  - $$ y = f(x)$$
- Usually, with real-world applications, we can at best appoximate the true mapping
  - $$ y = \hat{f(x)} + \epsilon $$
  - $\hat{f(x)}$ == approximate map
  - $\epsilon$ == irreducible error
- We want $\hat{f}$ to be as close to $f$ as possible (duh)

---
#### Loss Functions
- We can quantify the proximity of our appoximation through the use of a **loss function**
  - Two most common loss functions used in ML are the **0-1** or **Quadratic loss**
- Binary loss: classification
- Quadratic loss: regression
  - $$ L(f(x),\hat{f(x)}) = (f(x) - \hat{f(x)})^2$$
  - $$MSE = \frac 1 n \sum_{i=1}^{n} L(y_i,\hat{f(x_i)})^2$$
  - Having a low training error (MSE) does not guarnatee low test error in general.
- The closer to 0 for the test set the mo' betta.

---
#### Parametric v non-Parametric models
- Parametric : fixed number of inputs/parameters
  - With an algorithim, we learn to "tune" these parameters.
- Non-Parametric: Either infinite inputs or a variable number of parameters.
- Underfitting: Not enough parameters. Results in a model that is insufficiently complex.
- Overfitting: Too many parameters. Results in an excessively complex model.