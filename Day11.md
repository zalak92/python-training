# Day 11: Scikit-learn: Simple Model Training

## 11.1 Import Libraries

```python
from sklearn.linear_model import LinearRegression

11.2 Training a Model

import numpy as np
X = np.array([[1], [2], [3]])
y = np.array([2, 4, 6])
model = LinearRegression()
model.fit(X, y)
print(model.predict([[4]]))  # Predict for new data

11.3 Practice

    Train a linear regression model on any small dataset.
    Try predicting a new value.
