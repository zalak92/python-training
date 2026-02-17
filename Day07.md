# Day 7: Pandas Basics

## 7.1 Introduction

- Pandas is for data manipulation and analysis.

## 7.2 DataFrame Creation

```python
import pandas as pd
data = {'Name': ['Alice', 'Bob'], 'Age': [25, 30]}
df = pd.DataFrame(data)
print(df)

7.3 DataFrame Operations

print(df['Name'])       # Access a column
print(df.describe())    # Summary statistics

7.4 Practice

    Create a DataFrame with columns: ‘AI_Field’, ‘Years’, ‘Interest_Level’.
