# Data-Sampling-using-Python

Certainly! In Python, you can perform data sampling using various libraries such as NumPy, pandas, or scikit-learn. Below, I'll provide a brief explanation of how you might perform random sampling and stratified sampling using these libraries:

### Random Sampling:

**Using NumPy:**
```python
import numpy as np

# Assuming you have a dataset 'data'
data = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10])

# Perform random sampling
sample_size = 5
random_sample = np.random.choice(data, size=sample_size, replace=False)

print("Random Sample:", random_sample)
```

**Using pandas:**
```python
import pandas as pd

# Assuming you have a DataFrame 'df' with a column 'column_name'
df = pd.DataFrame({'column_name': [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]})

# Perform random sampling
sample_size = 5
random_sample = df['column_name'].sample(n=sample_size, replace=False)

print("Random Sample:", random_sample.tolist())
```

### Stratified Sampling:

**Using scikit-learn:**
```python
from sklearn.model_selection import train_test_split

# Assuming you have features 'X' and labels 'y'
X, y = np.array([[1, 2], [2, 3], [3, 4], [4, 5]]), np.array([0, 0, 1, 1])

# Perform stratified sampling
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.25, stratify=y)

print("Stratified X_train:", X_train)
print("Stratified y_train:", y_train)
print("Stratified X_test:", X_test)
print("Stratified y_test:", y_test)
```

In the stratified sampling example above, `stratify=y` ensures that the distribution of the target variable 'y' is maintained in both the training and testing sets.

These are just basic examples, and you may need to adapt the code to your specific dataset and requirements. Data sampling methods and parameters can vary based on the characteristics of your data and the objectives of your analysis or machine learning task.

