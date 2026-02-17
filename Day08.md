# Day 8: Data Loading & Preprocessing

## 8.1 Reading CSV

```python
import pandas as pd
df = pd.read_csv('data.csv')
print(df.head())

8.2 Handling Missing Data

df.fillna(0)    # Replace missing values with 0
df.dropna()     # Drop rows with missing values

8.3 Practice

    Load a sample CSV file (use any small CSV).
    Fill missing values with zero.
