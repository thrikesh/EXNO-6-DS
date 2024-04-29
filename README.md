# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
```python
import seaborn as sns
import matplotlib.pyplot as plt
x=[1,2,3,4,5]
y=[2,3,7,1,5]
sns.lineplot(x=x,y=y)
```

```python
sns.lineplot(x="total_bill",y="tip",data=df,hue="sex",linestyle="solid",legend="auto")
```
![image](https://github.com/MeethaPrabhu/EXNO-6-DS/assets/119401038/744968ca-2a33-43fe-bf08-a0d6a70f7fb5)

```python
import matplotlib.pyplot as plt
tips=sns.load_dataset('tips')
avg_total_bill=tips.groupby('day')['total_bill'].mean()
avg_tip=tips.groupby('day')['tip'].mean()

plt.figure(figsize=(8,6))
p1=plt.bar(avg_total_bill.index,avg_total_bill,label="Total Bill")
p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip')
plt.xlabel('Day of the week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by day')
plt.legend()
```
![image](https://github.com/MeethaPrabhu/EXNO-6-DS/assets/119401038/1c8702b1-678e-4704-b1c2-f5e4f58858e8)
```python
sns.barplot(x='day',y='total_bill',hue='sex',data=df,palette='Set2')
plt.xlabel('Day of the week')
plt.ylabel('Total Bill')
plt.title('Total Bill by day and gender')
```
![image](https://github.com/MeethaPrabhu/EXNO-6-DS/assets/119401038/8b6ebdad-5fed-4cc4-b04a-d0c469ca99a8)

```python
import seaborn as sns
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill',y='tip',hue='sex',data=tips)
plt.xlabel('Total Bill')
plt.ylabel('Tip Amount')
plt.title('Scatter plot of total bill vd Tip amount')
```
![image](https://github.com/MeethaPrabhu/EXNO-6-DS/assets/119401038/9cf8eb81-08ca-4fa0-822a-d9fd805b5264)

```python
import seaborn as sns
import numpy as np
import pandas as pd
num_var=pd.read_csv("/content/titanic_dataset.csv")
num_var
sns.histplot(data=num_var,x="Pclass",hue="Survived",kde=True)
```
![image](https://github.com/MeethaPrabhu/EXNO-6-DS/assets/119401038/c04fd9ff-9763-41f5-9baf-40fee16a6bbe)

```python
np.random.seed(1)
num=np.random.randn(100)
num=pd.Series(num,name="Numerical Variable")
num
sns.histplot(data=num,kde=True)
```
![image](https://github.com/MeethaPrabhu/EXNO-6-DS/assets/119401038/576530fb-71d8-4ac9-8392-ae86aad4bf78)

```python
import matplotlib.pyplot as plt
np.random.seed(0)
marks=np.random.normal(loc=70,scale=10,size=100)
marks
sns.histplot(data=marks,bins=10,kde=True,stat="count",cumulative=False,multiple="stack",element="bars",palette="Set1",color="black",shrink=0.7)
plt.xlabel('Marks')
plt.ylabel('Density')
plt.title('Histogram of students marks')
```
![image](https://github.com/MeethaPrabhu/EXNO-6-DS/assets/119401038/347fe8ae-e9db-4e73-bfa5-02188b12f470)

```python
import seaborn as sns
import pandas as pd
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'],y=tips['total_bill'],hue=tips['sex'])
```
![image](https://github.com/MeethaPrabhu/EXNO-6-DS/assets/119401038/b44be239-52cb-4d68-a03d-9407f439452b)

```python
sns.boxplot(x='day',y='total_bill',hue='smoker',data=tips, linewidth=2,width=0.6, boxprops={'facecolor':'lightblue','edgecolor':'black'},whiskerprops={'color':'blue','linestyle':'--','linewidth':1.5},capprops={'color':'red','linestyle':'--','linewidth':1.5})
```
![image](https://github.com/MeethaPrabhu/EXNO-6-DS/assets/119401038/b2e3c978-ec50-4415-89ff-e52d08286103)

```python
import seaborn as sns
import matplotlib.pyplot as plt
tips=sns.load_dataset('tips')
sns.violinplot(x='day',y='total_bill',hue='smoker',data=tips, linewidth=2,width=0.6, palette='Set1',color='blue',inner="quartile")
plt.xlabel('Day of the week')
plt.ylabel('Total Bill')
plt.title('Violin plot of Total bill by day and smoker status')
```
![image](https://github.com/MeethaPrabhu/EXNO-6-DS/assets/119401038/63d2729d-db79-4016-8634-fb8847fc716d)


# RESULT:
The data visualization using seaborn is successfully implemented.
