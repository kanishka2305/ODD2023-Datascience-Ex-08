# Ex-08-Data-Visualization-
# AIM
To Perform Data Visualization on a complex dataset and save the data to a file.

# Explanation
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
```py
Developed br:Kanishka.V.s
Reg no:212222230061
```
```py
  import matplotlib.pyplot as plt
  x_values=[0,1,2,3,4,5]
  y_values=[0,1,4,9,16,25]
  plt.plot(x_values,y_values)
```
![image](https://github.com/kanishka2305/ODD2023-Datascience-Ex-08/assets/113497357/7c5d1a01-0782-4ef9-905c-46d529f08a35)
```py
x=[1,2,3]
y=[2,4,1]
plt.plot(x,y)
plt.xlabel('x-values')
plt.ylabel('y-values')
plt.title('My first graph')
```
![image](https://github.com/kanishka2305/ODD2023-Datascience-Ex-08/assets/113497357/b1b9b499-707a-456d-8935-fbc51c1ac78c)
```py
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
![image](https://github.com/kanishka2305/ODD2023-Datascience-Ex-08/assets/113497357/d43aeb7c-18a5-47e2-a894-eea57fbe3433)
```py
x=[1,2,3,4,5,6]
y=[2,4,1,5,2,6]

plt.plot(x,y,color='green',linestyle='dashed',linewidth=3,marker='o',markerfacecolor='blue',markersize=12)
plt.ylim(1,8)
plt.xlim(1,8)
plt.xlabel('x-values')
plt.ylabel('y-values')
plt.title('some cool customizations')
```
![image](https://github.com/kanishka2305/ODD2023-Datascience-Ex-08/assets/113497357/af4098a1-4dac-4fc6-a60a-c35f2d9ad97a)
```py
yield_apples=[0.8,0.91,0.919,0.926,0.929,0.93]
plt.plot(yield_apples)
```
![image](https://github.com/kanishka2305/ODD2023-Datascience-Ex-08/assets/113497357/127896b8-d299-48a7-bc1d-2d52bafd747e)
```py
years=[2010,2011,2012,2013,2014,2015]
yield_apples=[0.895,0.91,0.919,0.926,0.929,0.931]
plt.plot(years,yield_apples)
```
![image](https://github.com/kanishka2305/ODD2023-Datascience-Ex-08/assets/113497357/7d960ad1-62f9-4697-b6ef-b8faf64f2428)
```py

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

![image](https://github.com/kanishka2305/ODD2023-Datascience-Ex-08/assets/113497357/12c23dac-baa3-4daf-ba8a-7d0e138dca7b)
```py
import seaborn as sns
import matplotlib.pyplot as plt

x=[1,2,3,4,5]
y=[3,6,2,7,1]

sns.lineplot(x=x,y=y)
```

![image](https://github.com/kanishka2305/ODD2023-Datascience-Ex-08/assets/113497357/7ff4869d-a8c8-4129-986a-0fe860b032a7)
```py
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
![image](https://github.com/kanishka2305/ODD2023-Datascience-Ex-08/assets/113497357/f1b623be-4f1a-4164-824a-0ffd8ebadbc3)
```py
import matplotlib.pyplot as plt
values=[5,6,3,7,2]
names=["A","B","C","D","E"]
plt.bar(names,values,color="green")
plt.show()
```

![image](https://github.com/kanishka2305/ODD2023-Datascience-Ex-08/assets/113497357/1b18a49b-1ba9-4a83-be92-067c206a11df)
```py
plt.barh(names,values,color="black")
plt.show()
```

![image](https://github.com/kanishka2305/ODD2023-Datascience-Ex-08/assets/113497357/0ee186ca-1936-48bc-b9cc-f95bfc58d202)
```py
height=[10,24,36,40,5]
names=["one","two","three","four","five"]
c1=["red","green"]
c2=["b","g"]
plt.bar(names,height,width=0.8,color=c1)
plt.xlabel("x-axis")
plt.ylabel("y-axis")
plt.title("My Bar chart!!!!!!!!!!!!")
```
![image](https://github.com/kanishka2305/ODD2023-Datascience-Ex-08/assets/113497357/96f16667-14ba-4cb7-9e85-35ca6d506cd3)
```py
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

![image](https://github.com/kanishka2305/ODD2023-Datascience-Ex-08/assets/113497357/db2cd6b5-e2db-46f5-8577-0b15f2b282b6)
```py
import seaborn as sns
dt=sns.load_dataset("tips")
sns.barplot(x="day",y="total_bill",hue="sex",data=dt,palette="Set1")
plt.xlabel('Day of the Week')
plt.ylabel('Total bill')
plt.title("Total bill by day and gender")
```
![image](https://github.com/kanishka2305/ODD2023-Datascience-Ex-08/assets/113497357/dc316e4d-e456-4078-9611-398ab13acdcb)
```py
import pandas as pd
tit=pd.read_csv("/content/titanic_dataset.csv")

plt.figure(figsize=(8,5))
sns.barplot(x="Embarked",y="Fare",data=tit,palette="rainbow")
plt.title("Fare of passengers by embarked town")
```
![image](https://github.com/kanishka2305/ODD2023-Datascience-Ex-08/assets/113497357/b572f3fe-f6a8-4184-b56e-aaf2cdb19c7c)
```py
import matplotlib.pyplot as plt
x_values = [0,1,2,3,4,5]
y_values = [0,1,4,9,16,25]
plt.scatter (x_values, y_values, s=30, color="blue")
plt.show()
```

![image](https://github.com/kanishka2305/ODD2023-Datascience-Ex-08/assets/113497357/230757ab-430b-4e61-b3ec-c388f147e973)
```py
x = [1,2,3,4,5,6,7,8,9,10]
y = [2,4,5,7,6,8,9,11,12,12]
plt.scatter(x,y,label = "stars",color='green',marker='*',s=30)
plt.title("scatter plot")
plt.legend()
```

![image](https://github.com/kanishka2305/ODD2023-Datascience-Ex-08/assets/113497357/99decf80-58b7-4f44-894a-cdc6aa3ed07b)
```py
import seaborn as sns
tips = sns.load_dataset('tips')
sns.scatterplot(x= 'total_bill', y='tip', hue='sex',data=tips)
plt.xlabel('Total Bill')
plt.ylabel('Tip Amount')
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```

![image](https://github.com/kanishka2305/ODD2023-Datascience-Ex-08/assets/113497357/26d746cf-51c1-4e0c-9919-1fcc7341c47e)
```py
import matplotlib.pyplot as plt
ages=[2,5,70,40,30,45,50,45,43,40,44,60,7,13,57,18,90,77,32,21,20,40]
range=(0,100)
bins=10
plt.hist(ages,bins,range,color="green",histtype="bar",rwidth=0.8)
plt.xlabel("age")
plt.ylabel("No.of.People")
plt.title("My Histogram")
```

![image](https://github.com/kanishka2305/ODD2023-Datascience-Ex-08/assets/113497357/65b6ae5d-ae9d-48db-abdf-0163440ee90c)
```py
x=[2,1,6,2,4,2,4,8,9,4,2,4,10,6,4,5,7,7,3,2,7,5,3,5,9,2,1]
plt.hist(x,bins=10,color="black",alpha=0.5)
```

![image](https://github.com/kanishka2305/ODD2023-Datascience-Ex-08/assets/113497357/20c1ae3e-e883-4baf-95c7-6c92d3a1d5e4)
```py
import seaborn as sns
import numpy as np
import pandas as pd

np.random.seed(1)
num_var=np.random.randn(1000)
num_var=pd.Series(num_var,name="Numerical Variable")
num_var
```

![image](https://github.com/kanishka2305/ODD2023-Datascience-Ex-08/assets/113497357/a26d0405-e21c-431f-adc0-3d8ce87c61b0)
```py
sns.histplot(data=num_var,kde=True)
```
![image](https://github.com/kanishka2305/ODD2023-Datascience-Ex-08/assets/113497357/def81108-1d95-49a7-9e2f-02ed588e3e04)
```py
import pandas as pd
import seaborn as sns
df=pd.read_csv("/content/titanic_dataset.csv")

sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
![image](https://github.com/kanishka2305/ODD2023-Datascience-Ex-08/assets/113497357/3fa866e8-b1b4-4db3-905a-924d2cc0babe)
```py
import matplotlib.pyplot as plt
import numpy as np

np.random.seed(0)
data=np.random.normal(loc=0,scale=1,size=100)
data
```
![image](https://github.com/kanishka2305/ODD2023-Datascience-Ex-08/assets/113497357/7b932718-c0dc-4cb6-ba00-dbde04abf234)
```py
fig,ax=plt.subplots()
ax.boxplot(data)
ax.set_xlabel("Data")
ax.set_ylabel("Values")
ax.set_title("Boxplot")
```

![image](https://github.com/kanishka2305/ODD2023-Datascience-Ex-08/assets/113497357/a21d7c74-f832-426d-a5b5-dbdad671511c)
```py
import seaborn as sns
import pandas as pd
tips = sns.load_dataset('tips')
sns.boxplot(x=tips["day"], y=tips["total_bill"], hue=tips["smoker"], data = tips)
```

![image](https://github.com/kanishka2305/ODD2023-Datascience-Ex-08/assets/113497357/2a44a300-1eb2-4975-986d-c1389fc8bd51)
```py
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6,boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
whiskerprops={"color": "black", "linestyle":"--", "linewidth": 1.5 },capprops={"color": "black", "linestyle": "--", "linewidth":1.5})
```

![image](https://github.com/kanishka2305/ODD2023-Datascience-Ex-08/assets/113497357/e66685ad-b770-4eba-9d09-bc93d2913e63)
```py
sns.boxplot(x='day',y='total_bill',data= tips)
plt.title("Age by Passenger Class, Titanic")
```

![image](https://github.com/kanishka2305/ODD2023-Datascience-Ex-08/assets/113497357/3e0c38a2-a1d4-4f53-913a-51c3053ca27d)
```py
sns.violinplot (x="day", y="total_bill", hue="smoker", data= tips, linewidth=2, width=0.6,)
```

![image](https://github.com/kanishka2305/ODD2023-Datascience-Ex-08/assets/113497357/3f0c80cf-94b8-454f-821b-b4dcfc87ae05)
```py
data = np.random.randint(low = 1, high = 100, size = (10,10))
print("The data to be plotted: \n")
print (data)
```
![image](https://github.com/kanishka2305/ODD2023-Datascience-Ex-08/assets/113497357/a67398f4-c920-4b50-8130-567e2f523347)
```py
hm=sns.heatmap(data=data)
```

![image](https://github.com/kanishka2305/ODD2023-Datascience-Ex-08/assets/113497357/7ea71170-8334-4980-96ef-8f2527640c2e)
```py
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

![image](https://github.com/kanishka2305/ODD2023-Datascience-Ex-08/assets/113497357/779b6b85-14f0-452b-8019-3a3ce6674898)

# Result:
Hence the data visualization method for the given dataset applied successfully.
