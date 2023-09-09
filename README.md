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

![image](https://github.com/vinushcv/Ex03-Univariate-Analysis/assets/113975318/a0b3e571-780a-4926-8ceb-8640bf449b09)

![image](https://github.com/vinushcv/Ex03-Univariate-Analysis/assets/113975318/d55d9ad0-a1f7-48f4-b2dd-8d3c1a37d4c8)

![image](https://github.com/vinushcv/Ex03-Univariate-Analysis/assets/113975318/e5fb0998-c333-444d-88f1-eb4ba6cfd627)

```python
sns.countplot(x='species',data=df)
```
![image](https://github.com/vinushcv/Ex03-Univariate-Analysis/assets/113975318/c07d4e43-fb89-414d-9269-48c65b2fc770)

```python
dfv=df.loc[df['species']=='virginica']

plt.plot(dfv['sepal_length'],np.zeros_like(dfv['sepal_length']),'*')
plt.xlabel('sepal length')
plt.show()
```
![image](https://github.com/vinushcv/Ex03-Univariate-Analysis/assets/113975318/0f50d6ad-9096-4f7d-ad33-d1ab8362e16b)

```python
dfs=df.loc[df['species']=='setosa']
dfc=df.loc[df['species']=='versicolor']

plt.plot(dfs['sepal_length'],np.zeros_like(dfs['sepal_length']),'*')
plt.plot(dfc['sepal_length'],np.zeros_like(dfc['sepal_length']),'X')
```
![image](https://github.com/vinushcv/Ex03-Univariate-Analysis/assets/113975318/fd354dea-b648-48bb-a922-d1f003907fec)

```python
plt.plot(dfv['sepal_length'],np.zeros_like(dfv['sepal_length']),'o')
plt.plot(dfs['sepal_length'],np.zeros_like(dfs['sepal_length']),'*')
plt.plot(dfc['sepal_length'],np.zeros_like(dfc['sepal_length']),'X')
plt.xlabel('petal_length')
plt.show()
```
![image](https://github.com/vinushcv/Ex03-Univariate-Analysis/assets/113975318/06335ff4-ede2-456c-9200-68a93d3ce1b5)

```python
plt.plot(dfv['sepal_length'],np.zeros_like(dfv['sepal_length']),'o')
plt.plot(dfs['sepal_length'],np.zeros_like(dfs['sepal_length']),'+')
plt.plot(dfc['sepal_length'],np.zeros_like(dfc['sepal_length']),'-')
plt.xlabel('SEPALLENGTH')
plt.show()
```
![image](https://github.com/vinushcv/Ex03-Univariate-Analysis/assets/113975318/474df709-025a-4baa-840a-1a7a97f2fec7)

### Result:
The given datasets are read and outliers are detected and are removed using IQR and z-score methods.











