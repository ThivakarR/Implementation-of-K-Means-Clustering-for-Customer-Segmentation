# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import pandas and matplot libraries.

2.import Kmeans algorithm to solve customer segmentation.

3.Using the for loop cluster the given data

4.Predict the output and plot data graphs. 5.Display the outputs. 

## Program:

```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: R.Thivakar
RegisterNumber:  212222240109
import pandas as pd
import matplotlib.pyplot as plt
data=pd.read_csv("/content/Mall_Customers.csv")
print('data.head():')
data.head()
print('data.info():')
data.info()
print('isnull() and sum():')
data.isnull().sum()
from sklearn.cluster import KMeans
wcss = []
for i in range(1,11):
  kmeans=KMeans(n_clusters=i,init="k-means++")
  kmeans.fit(data.iloc[:,3:])
  wcss.append(kmeans.inertia_)
print('Elbow method diagram:')
plt.plot(range(1,11),wcss)
plt.xlabel("No. of Clusters")
plt.ylabel("wcss")
plt.title("Elbow Method")
print('KMeans():')
km=KMeans(n_clusters=5)
km.fit(data.iloc[:,3:])
print('array():')
y_pred=km.predict(data.iloc[:,3:])
y_pred
print('Customer segments diagram:')
data["cluster"] = y_pred
df0 = data[data["cluster"]==0]
df1 = data[data["cluster"]==1]
df2 = data[data["cluster"]==2]
df3 = data[data["cluster"]==3]
df4 = data[data["cluster"]==4]
plt.scatter(df0["Annual Income (k$)"],df0["Spending Score (1-100)"],c="red",label="cluster0")
plt.scatter(df1["Annual Income (k$)"],df1["Spending Score (1-100)"],c="black",label="cluster1")
plt.scatter(df2["Annual Income (k$)"],df2["Spending Score (1-100)"],c="blue",label="cluster2")
plt.scatter(df3["Annual Income (k$)"],df3["Spending Score (1-100)"],c="green",label="cluster3")
plt.scatter(df4["Annual Income (k$)"],df4["Spending Score (1-100)"],c="magenta",label="cluster4")
plt.legend()
plt.title("Customer segments")

*/
```

## Output:
![K Means Clustering for Customer Segmentation](sam.png)

![240796731-fbcd1e35-2b91-409d-8546-b6102ce69f5a](https://github.com/Bala1511/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/118680410/98c8a18e-f34d-4b18-9945-d41abcbf3bab)

![240796776-64e275e0-462c-46c9-bd2a-f96fdd1818d3](https://github.com/Bala1511/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/118680410/90783ab2-897f-4caa-9d82-09515bfca3bb)


![240796821-9fe28a96-e0a8-4abc-8a27-95b5a3b09639](https://github.com/Bala1511/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/118680410/b66e1b49-29ff-4485-83de-fd6fa4788189)

![240796916-6b27e53c-1add-4d42-95a2-df3ac9b0d118](https://github.com/Bala1511/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/118680410/0d5ab68f-fa96-4814-9920-a1109db870dd)

![240797191-9323f6c6-621c-4cff-b1cc-d67f65599482](https://github.com/Bala1511/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/118680410/16527aff-8810-43cc-9cc4-27972a5ff8cc)

![240797238-6d79e92c-5cf3-4693-b4f4-26e88c28b53f](https://github.com/Bala1511/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/118680410/73fe1d2e-5ca9-41cf-bde8-cd169cd3e2a0)

![240797330-ab96f875-937f-4820-8933-84b7489085a4](https://github.com/Bala1511/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/118680410/6e64108d-5ecb-4554-b896-d615c9330d7a)

## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
