## Model Interpretation and Decision Boundary Analysis

### Interpreting Learned Coefficients

After training, the logistic regression model provides a set of learned weights (coefficients) for each input feature, along with a bias term. These coefficients represent the strength and direction of each feature's influence on the predicted probability of the positive class:

- **Positive Coefficient**: Indicates that as the feature value increases, the likelihood of the positive class increases.
- **Negative Coefficient**: Suggests that higher values of the feature decrease the likelihood of the positive class.
- **Magnitude**: The larger the absolute value of a coefficient, the more influential that feature is in the decision-making process.

By examining the printed weights, we can identify which features are most predictive and how they contribute to the classification boundary.

---

### Understanding the Decision Boundary

In logistic regression, the decision boundary is defined by the equation:

\[
\mathbf{w} \cdot \mathbf{x} + b = 0
\]

Where:
- \(\mathbf{w}\) is the vector of learned weights,
- \(\mathbf{x}\) is the input feature vector,
- \(b\) is the bias term.

This equation defines a hyperplane in the feature space that separates the two classes. For a 3-feature dataset, this boundary is a 2D plane in 3D space. The model predicts class `1` for points on one side of the plane (where the sigmoid output ≥ 0.5) and class `0` for points on the other.

Because the dataset was generated with high class separability (`class_sep=2.0`), the decision boundary is expected to cleanly divide the two classes with minimal overlap. The effectiveness of this separation is reflected in the high accuracy, precision, and recall observed during evaluation.
