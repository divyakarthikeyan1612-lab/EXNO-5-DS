# EXNO-5-DS-DATA VISUALIZATION USING MATPLOT LIBRARY

# Aim:
  To Perform Data Visualization using matplot python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
```
import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt
from scipy.interpolate import make_interp_spline
x_values=[0,1,2,3,4,5]
y_values=[0,1,4,9,16,25]
plt.plot(x_values,y_values)
plt.show()
```

<img width="1389" height="763" alt="image" src="https://github.com/user-attachments/assets/7d477af3-6616-41ef-b76c-52ade9d6bd27" />


```
x = [1, 2, 3, 4, 5]
y = [3, 6, 2, 7, 1]
plt.plot(x, y, label="Line Graph", color="blue", marker="o")
plt.xlabel("X Axis")
plt.ylabel("Y Axis")
plt.legend()
plt.title("Simple Line Graph")
plt.show()
```

<img width="1390" height="758" alt="image" src="https://github.com/user-attachments/assets/f958cd76-ca64-479e-8e52-ef6b880d3557" />

```
x1 = [1,2,3]
y1 = [2,4,1]
x2 = [1,2,3]
y2 = [4,1,3]
plt.plot(x1, y1, label="line 1", color="red")
plt.plot(x2, y2, label="line 2", color="green")
plt.scatter(x1, y1, color="red")
plt.scatter(x2, y2, color="green")
plt.xlabel("X Axis")
plt.ylabel("Y Axis")
plt.legend()
plt.title("Two Line Graph")
plt.show()
```

<img width="1383" height="771" alt="image" src="https://github.com/user-attachments/assets/98273ffe-6e65-4ebb-8486-a00cbec749a7" />


```
x=[1,2,3,4,5,6]
y=[2,4,1,5,2,6]
plt.plot(x,y,color='green',linestyle='dashed',linewidth=3,marker='o',markerfacecolor='blue') 
plt.ylim(1,8)
plt.xlim(1,8)
plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.title('Some cool customizations')
plt.show()
```

<img width="1385" height="756" alt="image" src="https://github.com/user-attachments/assets/c7ae5987-b593-4b91-a0dc-79ca1b942e0b" />


```
x_values = [0,1,2,3,4,5]
y_values = [0,1,4,9,16,25]
plt.plot(x_values, y_values)
plt.fill_between(x_values, y_values, color="lightblue", alpha=0.5)
plt.title("Fill Between Graph")
plt.show()
```

<img width="1383" height="714" alt="image" src="https://github.com/user-attachments/assets/762d216d-4718-45e7-8b89-e092fffde114" />


```
x = np.array([1,2,3,4,5,6,7,8,9,10])
y = np.array([2,4,5,7,8,8,9,10,11,12])
x_new = np.linspace(x.min(), x.max(), 300)
spl = make_interp_spline(x, y, k=3)
y_smooth = spl(x_new)
plt.plot(x_new, y_smooth)
plt.title("Smooth Curve")
plt.show()
```

<img width="1385" height="755" alt="image" src="https://github.com/user-attachments/assets/6aff4a55-6351-4ce8-b003-7e31725c6c4a" />


```
values = [5, 6, 3, 7, 2]
names  = ["A", "B", "C", "D", "E"]
plt.bar(names, values, color='orange')
plt.xlabel("Names")
plt.ylabel("Values")
plt.title("Bar Graph")
plt.show()
```

<img width="1385" height="763" alt="image" src="https://github.com/user-attachments/assets/10214927-c48a-4722-91b4-5b65aeb6f095" />


```
c1 = ['red', 'green', 'blue', 'yellow', 'purple']
plt.bar(names, values, color=c1)
plt.show()
```


<img width="1389" height="622" alt="image" src="https://github.com/user-attachments/assets/295545b9-d03f-4f10-af37-68a3cf2941e6" />

```
df = sns.load_dataset("tips")
avg_total_bill = df.groupby("day")["total_bill"].mean()
avg_tip = df.groupby("day")["tip"].mean()
plt.figure(figsize=(8, 6))
p1 = plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill')
p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip')
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
plt.show()
```
<img width="1374" height="159" alt="image" src="https://github.com/user-attachments/assets/da324c25-19b0-4635-bffd-be195d8e09dd" />

<img width="1368" height="783" alt="image" src="https://github.com/user-attachments/assets/4eaef070-80a1-4ac5-9976-3cc31a5d37bb" />


```
x_values = [0,1,2,3,4,5]
y_values = [0,1,4,9,16,25]
plt.scatter(x_values, y_values)
plt.title("Scatter Plot")
plt.show()
```

<img width="1354" height="686" alt="image" src="https://github.com/user-attachments/assets/36911c24-7f5d-46c6-bddd-2186b83dc24c" />


```
x = [1,2,3,4,5,6,7,8,9,10]
y = [2,4,5,7,6,8,9,11,12,12]
plt.scatter(x, y, label="stars", color="green", marker="*", s=30)
plt.xlabel("X Axis")
plt.ylabel("Y Axis")
plt.title("Scatter Plot with Stars")
plt.legend()
plt.show()
```

<img width="1394" height="750" alt="image" src="https://github.com/user-attachments/assets/f3a5f5bd-e886-454f-8636-7938119126e4" />

```

activities = ['eat', 'sleep', 'work', 'play']
slices = [3, 7, 8, 6]
colors = ['r', 'y', 'g', 'b']
plt.pie(slices, labels=activities, colors=colors, autopct='%1.1f%%', startangle=90)
plt.title("Pie Chart")
plt.show()
```

<img width="1396" height="688" alt="image" src="https://github.com/user-attachments/assets/d3fc8ac2-8ea6-41af-a8c6-3e4c05252d93" />


```
x=np.arange(0,4*np.pi,0.1)
y=np.sin(x)
plt.title("sine wave form")
plt.plot(x,y)
plt.show()
```

<img width="1388" height="696" alt="image" src="https://github.com/user-attachments/assets/69956066-2cd6-49ac-8959-232c13b865d2" />

```
x=[1,2,3,4,5]
y1=[10,12,14,16,18]
y2=[5,7,9,11,13]
y3=[2,4,6,8,10]
plt.fill_between(x,y1,color='blue')
plt.fill_between(x,y2,color='green')
plt.plot(x,y1,color='red')
plt.plot(x,y2,color='black')
plt.legend(['y1','y2'])
plt.show()
```

<img width="1386" height="763" alt="image" src="https://github.com/user-attachments/assets/2e1de30a-e177-4684-8f68-08d6dae97596" />


```
plt.stackplot(x,y1,y2,y3,labels=['Line 1','Line 2','Line 3'])
plt.legend(loc='upper left')
plt.title('Stacked Line Chart')
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.show()
```

<img width="1383" height="741" alt="image" src="https://github.com/user-attachments/assets/ef4342f4-f446-40a8-855b-185686291abb" />


```
import numpy as np
import matplotlib.pyplot as plt
from scipy.interpolate import make_interp_spline
x=np.array([1,2,3,4,5,6,7,8,9,10])
y=np.array([2,4,5,7,8,8,9,10,11,12])
spl=make_interp_spline(x,y)
x_smooth=np.linspace(x.min(),x.max(),100)
y_smooth=spl(x_smooth)
plt.plot(x,y,'o',label='data')
plt.plot(x_smooth,y_smooth,'-',label='Spline')
plt.legend()
plt.show()
```

<img width="1386" height="778" alt="image" src="https://github.com/user-attachments/assets/6f587a51-ab04-4bab-9452-b849012d7805" />


```
values=[5,6,3,7,2]
names=["A","B","C","D","E"]
plt.barh(names,values,color="yellowgreen")
plt.show()
```

<img width="1391" height="643" alt="image" src="https://github.com/user-attachments/assets/f43bd3d3-90a0-47c7-87b2-9b2bf4a5b675" />


```
x=[2,8,10]
y=[11,16,9]
x2=[3,9,11]
y2=[6,15,7]
plt.bar(x,y,color='r')
plt.bar(x2,y2,color='g')
plt.title('Bar graph')
plt.ylabel('Y axis')
plt.xlabel('X axis')
plt.show()
```

<img width="1382" height="783" alt="image" src="https://github.com/user-attachments/assets/1ec3cbda-e6d6-48f9-ad8d-92b2e7ec545d" />


```
x=[2,1,6,4,2,4,8,9,4,2,4,10,6,4,5,7,7,3,2,7,5,3,5,9,2,1]
plt.hist(x,bins=10,color='blue',alpha=0.5)
plt.show()
```

<img width="1418" height="652" alt="image" src="https://github.com/user-attachments/assets/9fdb439e-42da-435e-90aa-edc4d33f7388" />


```
data = [42, 55, 67, 68, 70, 72, 75, 79, 81, 88, 95, 102, 140, 160]
plt.boxplot(data)
plt.title("Simple Boxplot")
plt.ylabel("Values")
plt.show()
```

<img width="1426" height="697" alt="image" src="https://github.com/user-attachments/assets/57aea8e3-a1dd-4899-84bf-88b120999d6c" />


# Result:
Thus, all the data visualization techniques of matplotlib has been implemented.
