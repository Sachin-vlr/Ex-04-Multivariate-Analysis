# Ex-04-Multivariate-Analysis
# AIM
To perform Multivariate EDA on the given data set.

# EXPLANATION
Exploratory data analysis is used to understand the messages within a dataset. This technique involves many iterative processes to ensure that the cleaned data is further sorted to better understand the useful meaning.The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.

# ALGORITHM
# STEP 1
Import the built libraries required to perform EDA and outlier removal.

# STEP 2
Read the given csv file

# STEP 3
Convert the file into a dataframe and get information of the data.

# STEP 4
Return the objects containing counts of unique values using (value_counts()).

# STEP 5
Plot the counts in the form of Histogram or Bar Graph.

# STEP 6
Use seaborn the bar graph comparison of data can be viewed.

# STEP 7
Find the pairwise correlation of all columns in the dataframe.corr()

# STEP 8
Save the final data set into the file

# PROGRAM:

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```
# BIVARIATE ANALYSIS
```python
sns.catplot(x="Gender",col="Survived",kind="count",data=dt,height=5, aspect=.7)

sns.catplot(x='Survived',hue = "Gender",data = dt,kind = "count")

fig, ax1 = plt.subplots(figsize=(8,5))
graph = sns.countplot(ax=ax1,data=dt,x="Survived",hue="Pclass",palette="rainbow")
graph.set_xticklabels(graph.get_xticklabels())
for p in graph.patches:
  height = p.get_height()
  graph.text(p.get_x()+p.get_width()/2, height + 20.8,height,ha="left")

dt.boxplot(column="Age",by="Survived")

sns.scatterplot(x = dt["Age"],y = dt["Fare"])
```

# MULTIVARAITE ANALYSIS
```python
fig, ax1 = plt.subplots(figsize = (8,5))
pt = sns.boxplot(ax = ax1,x = 'Pclass',y = 'Age', hue='Gender',data=dt)

sns.catplot(data=dt,col="Survived",x="Gender",hue ="Pclass",kind = "count")

g = sns.catplot(data=dt,col="Survived",x="Gender",hue ="Pclass",kind = "count",legend=True)
g.fig.set_size_inches(8,5)
g.fig.subplots_adjust(top=0.81,right=0.86)
ax = g.facet_axis(0,0)
for p in ax.patches:
  ax.text(p.get_x()- 0.01,p.get_height() * 1.02,'{0:.1f}'.format(p.get_height()),color='red',rotation='horizontal',size='small')

corr = dt.corr()
sns.heatmap(corr,annot=True)

sns.pairplot(dt)
```
# OUTPUT

![image](https://github.com/Sachin-vlr/Ex-04-Multivariate-Analysis/assets/113497666/f56e076f-38cc-4ca0-931c-acf5ca403f93)

![image](https://github.com/Sachin-vlr/Ex-04-Multivariate-Analysis/assets/113497666/b7e5b5f7-ca22-4368-acde-5e2223981653)

![image](https://github.com/Sachin-vlr/Ex-04-Multivariate-Analysis/assets/113497666/48a1e53d-a5d7-4414-83a4-f1d326be4566)

![image](https://github.com/Sachin-vlr/Ex-04-Multivariate-Analysis/assets/113497666/b4d53334-8c51-4081-83a8-685ca82f44d1)

![image](https://github.com/Sachin-vlr/Ex-04-Multivariate-Analysis/assets/113497666/4554df26-f19f-4396-909d-f4afa87b109a)

![image](https://github.com/Sachin-vlr/Ex-04-Multivariate-Analysis/assets/113497666/07c2dba2-058d-442c-b6e2-e55ba7d6abfd)

![image](https://github.com/Sachin-vlr/Ex-04-Multivariate-Analysis/assets/113497666/e152f9b0-1e67-4d81-a236-100d57326727)
  
![image](https://github.com/Sachin-vlr/Ex-04-Multivariate-Analysis/assets/113497666/e09e6c54-ef49-4363-9e4f-fbe162a99894)

![image](https://github.com/Sachin-vlr/Ex-04-Multivariate-Analysis/assets/113497666/080c0387-e4c0-4f54-9d29-4f8bd52ade5d)

![image](https://github.com/Sachin-vlr/Ex-04-Multivariate-Analysis/assets/113497666/f9858989-0dea-4bc8-b840-eb9a6d336144)

# RESULT:
Thus,The program has been Executed Successfully.


