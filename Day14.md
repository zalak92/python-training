# Day 14: Mini Project & Next Steps

## 14.1 Mini Project: Predict Housing Prices

- Use the scikit-learn `load_diabetes` dataset (or another small dataset).

```python
from sklearn.datasets import load_diabetes
from sklearn.linear_model import LinearRegression
from sklearn.model_selection import train_test_split
from sklearn.metrics import mean_squared_error

# Load dataset
data = load_diabetes()
X = data.data
y = data.target

# Split data
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

# Train model
model = LinearRegression()
model.fit(X_train, y_train)

# Predict
y_pred = model.predict(X_test)

# Evaluate
mse = mean_squared_error(y_test, y_pred)
print("Test MSE:", mse)

14.2 Practice

    Try the same with a classification dataset (load_iris).
    Think: What would you like to learn next? (Deep learning, NLP, Computer Vision?)

14.3 Next Steps

    Explore more advanced AI and ML topics.
    Try Kaggle competitions.
    Practice building projects!
