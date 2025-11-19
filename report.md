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

## Training Insights

- **Loss Curve:**
- The model tracks cost at each epoch, showing convergence behavior.
- **Interpretability:**
-  Feature weights and bias are printed post-training to understand feature influence.
