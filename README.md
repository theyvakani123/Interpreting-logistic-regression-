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

