## Synthetic Data Generation Report

### Dataset Configuration

The synthetic dataset was generated using `sklearn.datasets.make_classification` with the following parameters:

- **Total Samples:** `500`
- **Number of Features:** `3`
- **Informative Features:** `3` (all features contribute to class separation)
- **Redundant Features:** `0` (no linear combinations of informative features)
- **Clusters per Class:** `1` (each class forms a single cluster)
- **Class Separation:** `2.0` (high separability between classes)
- **Random State:** `42` (ensures reproducibility)

This configuration creates a well-separated binary classification problem ideal for evaluating logistic regression performance.

---

### Data Split

- **Training Set:** `80%` (400 samples)
- **Test Set:** `20%` (100 samples)
- **Split Strategy:** Stratified random split using `train_test_split` with `random_state=42`


## Model Performance Metrics

After training the custom logistic regression model for `1000` epochs with a learning rate of `0.01`, the following performance metrics were observed on the test set:

| Metric      | Value       |
|-------------|-------------|
| Accuracy    | *0.99*      |
| Precision   | *1.0*       |
| Recall      | *0.98*      |


---
## Learned Coefficients and Bias

After training, the logistic regression model produced the following weights and bias:

- **Feature 1:** Weight = `1.6959`
- **Feature 2:** Weight = `-0.0904`
- **Feature 3:** Weight = `-0.0814`
- **Bias:** `-0.2006`

### Interpretation

- **Feature 1** has a strong positive influence on the prediction. A higher value in this feature significantly increases the likelihood of the sample being classified as class `1`.
- **Feature 2** and **Feature 3** have small negative weights, indicating a slight inverse relationship with the target class. Their influence is minimal compared to Feature 1.
- The **bias term** (`-0.2006`) shifts the decision boundary slightly, adjusting the threshold at which the model predicts class `1`.

These coefficients define the model's decision boundary in the 3D feature space. Since Feature 1 dominates, the model relies heavily on it to separate the classes, which aligns with the synthetic data's informative structure.

## Training Insights

- **Loss Curve:**
- The model tracks cost at each epoch, showing convergence behavior.
- **Interpretability:**
-  Feature weights and bias are printed post-training to understand feature influence.
