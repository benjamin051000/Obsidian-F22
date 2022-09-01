# California District Median Housing Price

## Step 1: Frame Problem
1. How will model be used?
2. What is current solution (baseline model)?
3. Supervised, unsupervised, reinforcement learning?
4. Classification or regression?
5. Is data an incoming stream? Online? Batch learning?
6. How do you measure success?


# Pandas
Like Excel but in Python.

Read in data
```python
import pandas as pd
housing = pd.read("housing.csv")
```
See columns
```python
housing.columns # Shows all cols
housing["longitude"]
```
Convert to np array
```python
housing.to_numpy()
```
Info: Get quick info about 