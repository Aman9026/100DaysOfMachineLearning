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
