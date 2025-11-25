```
import pandas as pd

data = pd.read_csv("http://labfile.oss.aliyuncs.com/courses/764/three_class_data.csv", header=0)
data.head()

```

```
from sklearn.cluster import KMeans
from sklearn.metrics import silhouette_score
from matplotlib import pyplot as plt
%matplotlib inline

X = data[["x", "y"]]
score = []  # 建立模型

# 依次计算 2 到 12 类的轮廓系数
for i in range(10):
    model = KMeans(n_clusters=i+2)
    model.fit(X)
    score.append(silhouette_score(X, model.labels_))

plt.figure(figsize=(11, 5))
plt.subplot(1, 2, 1)
plt.scatter(data['x'], data['y'])
plt.subplot(1, 2, 2)
plt.plot(range(2, 12, 1), score)
```
![[Pasted image 20251125145009.png]]
```
model = KMeans(n_clusters=3)
model.fit(X)
plt.scatter(data['x'], data['y'], c=model.labels_)
```
![[Pasted image 20251125145145.png]]