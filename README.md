# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Start.

2.Load and explore customer data.

3.Use the Elbow Method to find the best number of clusters.

4.Perform clustering on customer data.

5.Plot clustered data to visualize customer segments.

6.End.
 

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by:VIMALA SAHANA W 
RegisterNumber: 212223040241


import pandas as pd
import matplotlib.pyplot as plt
from sklearn.cluster import KMeans 

data=pd.read_csv("Mall_Customers.csv")
data.head()
data.info()
data.isnull().sum()

wcss=[]
for i in range(1,11):
  kmeans=KMeans(n_clusters=i,init="k-means++")
  kmeans.fit(data.iloc[:,3:])
  wcss.append(kmeans.inertia_)
plt.plot(range(1,11),wcss)
plt.xlabel("No_of_Clusters")
plt.ylabel("wcss")
plt.title("Elbow Method")
km=KMeans(n_clusters=5)
km.fit(data.iloc[:,3:])
y_pred=km.predict(data.iloc[:,3:])
y_pred



data["cluster"]=y_pred
df0=data[data["cluster"]==0]
df1=data[data["cluster"]==1]
df2=data[data["cluster"]==2]
df3=data[data["cluster"]==3]
df4=data[data["cluster"]==4]
plt.scatter(df0["Annual Income (k$)"],df0["Spending Score (1-100)"],c="red",label="cluster0")
plt.scatter(df1["Annual Income (k$)"],df1["Spending Score (1-100)"],c="black",label="cluster1")
plt.scatter(df2["Annual Income (k$)"],df2["Spending Score (1-100)"],c="blue",label="cluster2")
plt.scatter(df3["Annual Income (k$)"],df3["Spending Score (1-100)"],c="green",label="cluster3")
plt.scatter(df4["Annual Income (k$)"],df4["Spending Score (1-100)"],c="magenta",label="cluster4")
plt.legend()
plt.title("Customer Segment")
*/
```

## Output:
![Screenshot 2024-10-26 162745](https://github.com/user-attachments/assets/a45eedf2-79f8-47fc-8de8-58bfa99261b2)
![Screenshot 2024-10-26 162904](https://github.com/user-attachments/assets/0c5eda55-63aa-4588-b95e-a4d60eabe4d6)
![Screenshot 2024-10-26 162912](https://github.com/user-attachments/assets/05e891bf-1bc5-4f1f-b907-13ccec9c8b9c)
![Screenshot 2024-10-26 162936](https://github.com/user-attachments/assets/2e3fbcfa-1275-4c7c-82ac-e919d29dba07)
![Screenshot 2024-10-26 162955](https://github.com/user-attachments/assets/afddfeff-088f-48e2-a21e-fff6248b79de)






## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
