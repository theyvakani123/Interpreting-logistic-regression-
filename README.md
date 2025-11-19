# Interpreting-logistic-regression

## Project Objective

The objective of this project is to implement a logistic regression model from scratch using NumPy and apply it to a synthetically generated binary classification dataset. This hands-on approach aims to:

- Deepen understanding of the mathematical foundations of logistic regression
- Demonstrate how gradient descent optimizes model parameters
- Visualize training loss and interpret learned coefficients
- Evaluate model performance using accuracy, precision, and recall
- Provide a transparent and educational alternative to using pre-built machine learning libraries

By building the model manually, this project reinforces core concepts in supervised learning, optimization, and model evaluation.

## Generate a Synthetic Binary Classification Dataset

Create a dataset with `500` samples and `3` features where the target variable is binary (`0` or `1`), and the classes are well-separated. This setup ensures that a logistic regression model can learn the decision boundary effectively and achieve high classification performance.

- make_classification gives you control over the complexity and separability of the data.
- class_sep=2.0 ensures the classes are not overlapping too much, which helps logistic regression perform better.

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
