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
- **Regression**: When $y \in \reals$ (**the label is a real-value**)
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
- The closer to 0 for the test set the mo' betta.

---
#### Parametric v non-Parametric models
- Parametric : fixed number of inputs/parameters
  - With an algorithim, we learn to "tune" these parameters.
- Non-Parametric: Either infinite inputs or a variable number of parameters.
- **Put in the picture from the slides of parametric models differences here**
  - Mean squared error graph:
    - Bottom line (gray line) is the **complexity** (MSE/Flexibility) for the training. As more data points are added, MSE becomes smaller. This makes sense.
    - But that doesn't mean that it's necessarily better.
    - Top (Red) line represents test data.
    - Notice that it has a dip, we want to be in the dip (when I dip you dip we dip)

---
### Bias Variance Tradeoff
- **Picture from slides go here again**
- Bias-Variance Tradeoff: U-shape phenomena in test MSE indicative of two competing properties of learned models: Bias and Variance
  - Low Dimensional: High Bias & Low Variance
  - High Dimensional: Low Bias & High Variance
- I zoned out for a minute here and went to play with my dog while the lecture played. He was talking about the above picture. 

---
### Unsupervised Learning
- k-means: k represents the number of clusters. Classify a new datum based on a nearest centroid criterion - this algo is called k-means.
- Basically identifying the center of mass for each given cluster.
- Given a new datapoint, we could identify which cluster the new datapoint is closest to.

---
### Confusion Matrix
- Confusion Matrix: table that is often used to describe the performance of a classification model on a set of test data for which the true values are known
  - X axis: Predicted Class
  - Y axis: Actual class
  - Example: False positive would be bottom left, True for predication, False for actual 