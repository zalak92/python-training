# Day 12: Model Evaluation & Metrics

## 12.1 Evaluating Models

- After training, check how well your model performs!

## 12.2 Common Metrics

- **Regression:** Mean Squared Error (MSE), R² Score
- **Classification:** Accuracy, Precision, Recall

## 12.3 Example: Regression Evaluation

```python
from sklearn.metrics import mean_squared_error, r2_score

y_true = [3, 5, 2.5, 7]
y_pred = [2.5, 5, 4, 8]

mse = mean_squared_error(y_true, y_pred)
r2 = r2_score(y_true, y_pred)

print("Mean Squared Error:", mse)
print("R² Score:", r2)

12.4 Example: Classification Evaluation

from sklearn.metrics import accuracy_score

y_true = [0, 1, 1, 0]
y_pred = [0, 0, 1, 1]

accuracy = accuracy_score(y_true, y_pred)
print("Accuracy:", accuracy)

12.5 Practice

    Train a model (any, even same as yesterday) and compute its accuracy or MSE.
