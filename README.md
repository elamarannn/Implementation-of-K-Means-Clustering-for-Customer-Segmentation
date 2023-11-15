# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the necessary packages using import statement.
2.Read the given csv file using read_csv() method and print the number of contents to be displayed using df.head().
3.Import KMeans and use for loop to cluster the data.
4.Predict the cluster and plot data graphs.
5.Print the outputs and end the program

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: Elamaran S E
RegisterNumber: 212222230036

import pandas as pd
import matplotlib.pyplot as plt
data=pd.read_csv("Mall_Customers.csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.cluster import KMeans
wcss = []
for i in range(1,11):
  kmeans = KMeans (n_clusters = i, init ="k-means++")
  kmeans.fit(data.iloc[:,3:])
  wcss.append(kmeans.inertia_)
plt.plot(range(1,11),wcss)
plt.xlabel("no of cluster")
plt.ylabel("wcss")
plt.title("Elbow Metthod")
km=KMeans(n_clusters=5)
km.fit(data.iloc[:,3:])
y_pred = km.predict(data.iloc[:,3:])
y_pred
data["cluster"]=y_pred
df0=data[data["cluster"]==0]
df1=data[data["cluster"]==1]
df2=data[data["cluster"]==2]
df3=data[data["cluster"]==3]
df4=data[data["cluster"]==4]
plt.scatter(df0["Annual Income (k$)"],df0["Spending Score (1-100)"],c="red",label="cluster0")
plt.scatter(df1["Annual Income (k$)"],df1["Spending Score (1-100)"],c="pink",label="cluster1")
plt.scatter(df2["Annual Income (k$)"],df2["Spending Score (1-100)"],c="green",label="cluster2")
plt.scatter(df3["Annual Income (k$)"],df3["Spending Score (1-100)"],c="blue",label="cluster3")
plt.scatter(df4["Annual Income (k$)"],df4["Spending Score (1-100)"],c="black",label="cluster4")
plt.legend()
plt.title("Customer Segments")

*/
```

## Output:
## Dataset:
![280512947-ed5b0fe2-4e98-43bd-9b21-f3468d493335](https://github.com/elamarannn/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/113497531/450c8f18-fadb-4d6f-b408-0b048ff13aa0)
## Dataset information:
![280512950-8d4aa9d8-45dd-4539-8271-f7da5d00dc99](https://github.com/elamarannn/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/113497531/03bccc13-a09c-4f69-9663-8aad0ecfcfab)
![280512954-f3c984b3-7e9b-4852-9552-a4026fbfd52d](https://github.com/elamarannn/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/113497531/f420c7d3-38b9-48d8-ae8d-0aca51d0a978)
## Elbow method graph (wcss vs each iteration):
![280512960-65a43453-3ac2-4bea-8187-97cb6cc060d1](https://github.com/elamarannn/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/113497531/becc265d-0cff-4040-a0ee-c951dd00ab8b)
## Cluster represnting customer segments-graph:
![280512965-5796e66a-5977-4d88-857d-822ee784388d](https://github.com/elamarannn/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/113497531/6f3ff0c8-a1db-48f9-b185-b160986ac1c5)

## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
