# Simple Linear Regression
```
y =  b + cx
```
**Load data into program: **
 ```
 dataset = pd.read_csv('filedb.csv')
 dataset
```
![](https://github.com/Aman9026/100DaysOfMachineLearning/blob/master/Data/Images/Simpledataset.png)

**Predictor (x):**

``` x = dataset['time']```

**Predicted (y):**

``` y = dataset['no']```

**Convert predictor(x) into 2D numpy array:**
```
 X = x.values.reshape(3,1)
 X.shape
(3, 1)

from sklearn.linear_model import LinearRegression
```
**Create model:**
```
model = LinearRegression()
```
**Trained model:**

```model.fit(X,y)```

**Predict future by model:**
```
model.predict(3)
array([30.])
```
**Coefficient:**
```
model.coef_
array([10.])
```
**y-intercept or bias or constant :**
```
model.intercept_
1.4210854715202004e-14  ~ 0
```
```
 import matplotlib.pyplot as plt
 import seaborn as sns
 sns.set()
```
**Create Graph:**
```
 plt.scatter(X,y)
 plt.xlabel('time')
 plt.ylabel('marks')
```
![](https://github.com/Aman9026/100DaysOfMachineLearning/blob/master/Data/Images/samplegraph.png)

```
 plt.plot(X,y, marker='o')
 plt.xlabel('time')
 plt.ylabel('marks')
```
![](https://github.com/Aman9026/100DaysOfMachineLearning/blob/master/Data/Images/samplegraph2.png)



**Save model to file:**
```
from sklearn.externals import joblib
joblib.dump(model, 'filesave.pk1')
```

**Load model from save file :**
```
>>> from sklearn.externals import joblib
>>> model = joblib.load('lr.pk1')
>>> model
>>> model.predict(7)
```
