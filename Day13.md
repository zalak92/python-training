# Day 13: Neural Networks with Keras/TensorFlow

## 13.1 What is a Neural Network?

- A model inspired by the human brain, used for deep learning tasks.

## 13.2 Keras: Simple Neural Network

```python
import numpy as np
from tensorflow import keras

# Example data (XOR)
X = np.array([[0,0], [0,1], [1,0], [1,1]])
y = np.array([0, 1, 1, 0])

model = keras.Sequential([
    keras.layers.Dense(4, input_dim=2, activation='relu'),
    keras.layers.Dense(1, activation='sigmoid')
])

model.compile(optimizer='adam', loss='binary_crossentropy', metrics=['accuracy'])
model.fit(X, y, epochs=100, verbose=0)

print("Predictions:", model.predict(X))

13.3 Practice

    Build a simple neural network for any small dataset (or try the above XOR example).
    Change number of neurons and see what happens.
