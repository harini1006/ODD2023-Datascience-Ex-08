# Ex-08-Data-Visualization-
# AIM
To Perform Data Visualization on a complex dataset and save the data to a file.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# ALGORITHM
## STEP 1
Read the given Data

## STEP 2
Clean the Data Set using Data Cleaning Process

## STEP 3
Apply Feature generation and selection techniques to all the features of the data set

## STEP 4
Apply data visualization techniques to identify the patterns of the data.

# CODE AND OUTPUT:
```
NAME : R . JOYCE BEULAH
REG NO : 212222230058
```
```
  import matplotlib.pyplot as plt
  x_values=[0,1,2,3,4,5]
  y_values=[0,1,4,9,16,25]
  plt.plot(x_values,y_values)
```
![image](https://github.com/JoyceBeulah/ODD2023-Datascience-Ex-08/assets/118343698/0a87e118-3ad6-4c04-9d96-a8472646fd87)

```
x=[1,2,3]
y=[2,4,1]
plt.plot(x,y)
plt.xlabel('x-values')
plt.ylabel('y-values')
plt.title('My first graph')
```
![image](https://github.com/JoyceBeulah/ODD2023-Datascience-Ex-08/assets/118343698/f1b63fae-e0e4-4871-aec1-9943f923985d)

```
x1=[1,2,3]
y1=[2,4,1]
x2=[1,2,3]
y2=[4,1,3]
plt.plot(x1,y1,label='line 1')
plt.plot(x2,y2,label='line 2')
plt.xlabel('x-values')
plt.ylabel('y-values')
plt.title('Two lines on same graph')
```
![image](https://github.com/JoyceBeulah/ODD2023-Datascience-Ex-08/assets/118343698/2bd29fce-d40d-4f46-aa7f-ab9549b06a76)

```
x=[1,2,3,4,5,6]
y=[2,4,1,5,2,6]

plt.plot(x,y,color='green',linestyle='dashed',linewidth=3,marker='o',markerfacecolor='blue',markersize=12)
plt.ylim(1,8)
plt.xlim(1,8)
plt.xlabel('x-values')
plt.ylabel('y-values')
plt.title('some cool customizations')
```
![image](https://github.com/JoyceBeulah/ODD2023-Datascience-Ex-08/assets/118343698/4646ca20-a032-4a0d-934c-b1ded0e220c5)

```
yield_apples=[0.8,0.91,0.919,0.926,0.929,0.93]
plt.plot(yield_apples)
```
![image](https://github.com/JoyceBeulah/ODD2023-Datascience-Ex-08/assets/118343698/e78ae91c-25f9-497f-9e4b-12e6fc4d4332)

```
years=[2010,2011,2012,2013,2014,2015]
yield_apples=[0.895,0.91,0.919,0.926,0.929,0.931]
plt.plot(years,yield_apples)
```
![image](https://github.com/JoyceBeulah/ODD2023-Datascience-Ex-08/assets/118343698/6b65f1fe-106d-43ee-a7c8-19600a561a5f)

```
x=[1,2,3,4,5]
y1=[10,12,14,16,18]
y2=[5,7,9,11,13]
y3=[2,4,6,8,10]
plt.fill_between(x,y1,color='blue')
plt.fill_between(x,y2,color='yellow')
plt.plot(x,y1,color='black')
plt.plot(x,y2,color='white')
plt.legend(['y1','y2'])
```
![image](https://github.com/JoyceBeulah/ODD2023-Datascience-Ex-08/assets/118343698/4c1776e8-9f37-4a30-88df-a361eab0cce6)

```
import seaborn as sns
import matplotlib.pyplot as plt

x=[1,2,3,4,5]
y=[3,6,2,7,1]

sns.lineplot(x=x,y=y)
```
![image](https://github.com/JoyceBeulah/ODD2023-Datascience-Ex-08/assets/118343698/61715f6e-1d9d-495b-a22b-60c169540e5f)

```
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]

sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title("Multi-Line Plot")
plt.xlabel("X Label")
plt.ylabel("Y Label")
```
![image](https://github.com/JoyceBeulah/ODD2023-Datascience-Ex-08/assets/118343698/38022cd1-2857-4e0f-925d-eee94764233a)

```
import matplotlib.pyplot as plt
values=[5,6,3,7,2]
names=["A","B","C","D","E"]
plt.bar(names,values,color="green")
plt.show()
```
![image](https://github.com/JoyceBeulah/ODD2023-Datascience-Ex-08/assets/118343698/49555c67-fd6d-48b2-bd58-5905dee5f6a3)

```
plt.barh(names,values,color="black")
plt.show()
```
![image](https://github.com/JoyceBeulah/ODD2023-Datascience-Ex-08/assets/118343698/b674f8aa-f344-4733-8ddb-70a7532fcabb)

```
height=[10,24,36,40,5]
names=["one","two","three","four","five"]
c1=["red","green"]
c2=["b","g"]
plt.bar(names,height,width=0.8,color=c1)
plt.xlabel("x-axis")
plt.ylabel("y-axis")
plt.title("My Bar chart!!!!!!!!!!!!")
```
![image](https://github.com/JoyceBeulah/ODD2023-Datascience-Ex-08/assets/118343698/b95d9674-00c3-425d-ba9b-04347d00fc97)

```
import seaborn as sns
import matplotlib.pyplot as plt
tips= sns.load_dataset("tips")
avg_total_bill = tips.groupby("day")['total_bill'].mean()
avg_tip =tips.groupby('day')['tip'].mean()
plt.figure(figsize=(8, 6))
p1 = plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill')
p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip')
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title("Average total bil and tip by day")
plt.legend()
```
![image](https://github.com/JoyceBeulah/ODD2023-Datascience-Ex-08/assets/118343698/7239d5f2-b476-4a52-83c9-3035958ecf8f)

```
import seaborn as sns
dt=sns.load_dataset("tips")
sns.barplot(x="day",y="total_bill",hue="sex",data=dt,palette="Set1")
plt.xlabel('Day of the Week')
plt.ylabel('Total bill')
plt.title("Total bill by day and gender")
```
![image](https://github.com/JoyceBeulah/ODD2023-Datascience-Ex-08/assets/118343698/3c88b680-9f0f-48e8-9107-489b74aff79f)

```
import pandas as pd
tit=pd.read_csv("/content/titanic_dataset.csv")

plt.figure(figsize=(8,5))
sns.barplot(x="Embarked",y="Fare",data=tit,palette="rainbow")
plt.title("Fare of passengers by embarked town")
```
![image](https://github.com/JoyceBeulah/ODD2023-Datascience-Ex-08/assets/118343698/5cc8b8be-81fe-4b3e-892a-a95f33d24459)

```
import matplotlib.pyplot as plt
x_values = [0,1,2,3,4,5]
y_values = [0,1,4,9,16,25]
plt.scatter (x_values, y_values, s=30, color="blue")
plt.show()
```
![image](https://github.com/JoyceBeulah/ODD2023-Datascience-Ex-08/assets/118343698/1d9fc886-d269-4fba-91cd-603ccb07c2b0)

```
x = [1,2,3,4,5,6,7,8,9,10]
y = [2,4,5,7,6,8,9,11,12,12]
plt.scatter(x,y,label = "stars",color='green',marker='*',s=30)
plt.title("scatter plot")
plt.legend()
```
![image](https://github.com/JoyceBeulah/ODD2023-Datascience-Ex-08/assets/118343698/8a12ffa3-fe00-4836-bcd0-32c8a872f11b)

```
import seaborn as sns
tips = sns.load_dataset('tips')
sns.scatterplot(x= 'total_bill', y='tip', hue='sex',data=tips)
plt.xlabel('Total Bill')
plt.ylabel('Tip Amount')
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```
![image](https://github.com/JoyceBeulah/ODD2023-Datascience-Ex-08/assets/118343698/f6af6118-738d-4259-b1b0-973286e226ff)

```
import matplotlib.pyplot as plt
ages=[2,5,70,40,30,45,50,45,43,40,44,60,7,13,57,18,90,77,32,21,20,40]
range=(0,100)
bins=10
plt.hist(ages,bins,range,color="green",histtype="bar",rwidth=0.8)
plt.xlabel("age")
plt.ylabel("No.of.People")
plt.title("My Histogram")
```
![image](https://github.com/JoyceBeulah/ODD2023-Datascience-Ex-08/assets/118343698/902264e3-d0be-4a23-8c4e-daf8e831b561)

```
x=[2,1,6,2,4,2,4,8,9,4,2,4,10,6,4,5,7,7,3,2,7,5,3,5,9,2,1]
plt.hist(x,bins=10,color="black",alpha=0.5)
```
![image](https://github.com/JoyceBeulah/ODD2023-Datascience-Ex-08/assets/118343698/60ff4330-040e-4dc8-a807-36345019f7bc)

```
import seaborn as sns
import numpy as np
import pandas as pd

np.random.seed(1)
num_var=np.random.randn(1000)
num_var=pd.Series(num_var,name="Numerical Variable")
num_var
```
![image](https://github.com/JoyceBeulah/ODD2023-Datascience-Ex-08/assets/118343698/753e65d1-40af-41b4-bf8c-ba59df0805b7)

```
sns.histplot(data=num_var,kde=True)
```
![image](https://github.com/JoyceBeulah/ODD2023-Datascience-Ex-08/assets/118343698/30e897b1-369c-4358-afb9-25b6522e5772)

```
import pandas as pd
import seaborn as sns
df=pd.read_csv("/content/titanic_dataset.csv")

sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
![image](https://github.com/JoyceBeulah/ODD2023-Datascience-Ex-08/assets/118343698/60142d6f-4a2c-4e10-b738-996176664dcd)

```
import matplotlib.pyplot as plt
import numpy as np

np.random.seed(0)
data=np.random.normal(loc=0,scale=1,size=100)
data
```
![image](https://github.com/JoyceBeulah/ODD2023-Datascience-Ex-08/assets/118343698/1eb619e6-7d84-46a5-99ce-1daff5947eca)

```
fig,ax=plt.subplots()
ax.boxplot(data)
ax.set_xlabel("Data")
ax.set_ylabel("Values")
ax.set_title("Boxplot")
```
![image](https://github.com/JoyceBeulah/ODD2023-Datascience-Ex-08/assets/118343698/2588914b-ca9c-4045-bf16-f59d57afc9e2)

```
import seaborn as sns
import pandas as pd
tips = sns.load_dataset('tips')
sns.boxplot(x=tips["day"], y=tips["total_bill"], hue=tips["smoker"], data = tips)
```
![image](https://github.com/JoyceBeulah/ODD2023-Datascience-Ex-08/assets/118343698/9154a693-bcd0-4ccc-bc8b-10e822c80d46)

```
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6,boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
whiskerprops={"color": "black", "linestyle":"--", "linewidth": 1.5 },capprops={"color": "black", "linestyle": "--", "linewidth":1.5})
```
![image](https://github.com/JoyceBeulah/ODD2023-Datascience-Ex-08/assets/118343698/e2abee05-8ddc-4986-95b5-6483196988da)

```
sns.boxplot(x='day',y='total_bill',data= tips)
plt.title("Age by Passenger Class, Titanic")
```
![image](https://github.com/JoyceBeulah/ODD2023-Datascience-Ex-08/assets/118343698/b0301188-304a-4119-bf3a-715389262274)

```
sns.violinplot (x="day", y="total_bill", hue="smoker", data= tips, linewidth=2, width=0.6,)
```
![image](https://github.com/JoyceBeulah/ODD2023-Datascience-Ex-08/assets/118343698/abcaf8b3-3260-4ac9-854a-09d6e66a1305)

```
data = np.random.randint(low = 1, high = 100, size = (10,10))
print("The data to be plotted: \n")
print (data)
```
![image](https://github.com/JoyceBeulah/ODD2023-Datascience-Ex-08/assets/118343698/418810af-4f2b-4a21-94cb-5846543bec26)

```
hm=sns.heatmap(data=data)
```
![image](https://github.com/JoyceBeulah/ODD2023-Datascience-Ex-08/assets/118343698/4e98eb1c-912e-42a2-969c-887a52943a5a)

```
import pandas as pd
import seaborn as sns
df=pd.read_csv("/content/titanic_dataset.csv")

import matplotlib.pyplot as plt
ages= [2,5, 70, 40, 30, 45, 50,45, 43, 40,44, 60, 7,13, 57, 18, 90, 77,32, 21, 20, 40]
range = (0, 100)
bins = 10
sns.histplot(data=df,x="Pclass",hue="Survived")
plt. xlabel ('age')
plt.ylabel ('No. of people')
plt. title ('My histogram')
plt.show()
```
![image](https://github.com/JoyceBeulah/ODD2023-Datascience-Ex-08/assets/118343698/78091e0a-cc8e-4105-9141-40f67c4ee72c)

# RESULT:
Hence the data visualization method for the given dataset applied successfully.
