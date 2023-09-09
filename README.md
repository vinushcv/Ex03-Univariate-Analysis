# Ex03-Univariate-Analysis
### Aim
To read the given data and perform the univariate analysis with different types of plots.
### Explanation
Univariate analysis is basically the simplest form to analyze data. Uni means one and this means that the data has only one kind of variable. The major reason for univariate analysis is to use the data to describe. The analysis will take data, summarise it, and then find some pattern in the data.
### Algorithm
## step 1:
Read the given data.
## step 2:
Get the information about the data.
## step 3:
Remove the null values from the data.
## step 4:
Mention the datatypes from the data.
## step 5:
Count the values from the data.
## step 6:
Do plots like boxplots,countplot,distribution plot,histogram plot.
### Program:
name:vinushcv
registration number:212222230176
```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

df=pd.read_csv("/content/iris (1).csv")

df.nunique()
```
![image](https://github.com/vinushcv/Ex03-Univariate-Analysis/assets/113975318/eb3c1e61-4302-4b62-b9c9-37d35492a7c2)

```python
df.head()
```

![image](https://github.com/vinushcv/Ex03-Univariate-Analysis/assets/113975318/9176b92c-f037-4cd5-be13-6677d94e66a8)

```python
df.tail()
```

![image](https://github.com/vinushcv/Ex03-Univariate-Analysis/assets/113975318/e991eed3-eba9-4a24-816f-741926d3c0e3)

```python
df.iloc[:,4].value_counts()
```
![image](https://github.com/vinushcv/Ex03-Univariate-Analysis/assets/113975318/266ce04f-db30-435a-acd0-b85212fc7aa6)

```python
for i in range(0,df.shape[1]):
  print("-----------",df.columns[i],"------------")
  print(df.iloc[:,i].value_counts())
  print("---------------------------------------")
```
![image](https://github.com/vinushcv/Ex03-Univariate-Analysis/assets/113975318/829bb76c-13e6-452a-9701-6c1fc98d6097)



