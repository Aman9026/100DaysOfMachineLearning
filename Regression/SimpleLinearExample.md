# Salary Prediction model using simple linear regression
```
>>> import pandas as pd
>>> dataset = pd.read_csv('SalaryData.csv')
>>> dataset.head()
```
![](https://github.com/Aman9026/100DaysOfMachineLearning/blob/master/Data/Images/datasetex.png)

```
>>> X = dataset.iloc[: , 0:1].values
>>> y = dataset.iloc[: , 1].values
>>> from sklearn.model_selection import train_test_split
>>> X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.30, random_state=42)
>>> from sklearn.linear_model import LinearRegression
>>> model = LinearRegression()
>>> model.fit(X_train, y_train)
>>> y_pred = model.predict(X_test)
```
```
>>> y_test
array([112635.,  67938., 113812.,  83088.,  64445.,  57189., 122391.,
       109431.,  56957.])
```
```
>>> y_pred
array([115573.62288352,  71679.93878159, 102498.90847018,  75415.57147111,
        55803.4998511 ,  60473.04071301, 122110.98009019, 107168.44933209,
        63274.76523015])
```
```
>>> import matplotlib.pyplot as plt
>>> import seaborn as sns
>>> sns.set()
```
```
>>> plt.scatter(X_test, y_test, color='red')
>>> plt.plot(X_test, y_pred)
>>> plt.title('Salary vs Exp Prediction')
>>> plt.xlabel('Exp')
>>> plt.ylabel('Salary')
>>> plt.show()
```
## Draw best fit line
![](https://github.com/Aman9026/100DaysOfMachineLearning/blob/master/Data/Images/expgraph.png)
```
>>> from sklearn import  metrics
>>> print("MAE: ", metrics.mean_absolute_error(y_test , y_pred))
>>> print("MSE: ", metrics.mean_squared_error(y_test, y_pred))
>>> import numpy as np
>>> print("RMSE: " , np.sqrt(metrics.mean_squared_error(y_test, y_pred)))
```
```
>>> from sklearn.externals import joblib
>>> joblib.dump(model, 'salary.pk1')
```
## Create App for salary Estimator uses by other User:

Create file from text editor, save content in salary_app.py:

```
from sklearn.externals import joblib
model = joblib.load('salary.pk1')
exp= input("Enter exp: ")
exp = int(exp)
salary_predict = model.predict(exp)
print("Estimated Salary: " , salary_predict[0])
```

### Run above created file:
```
>python salary_app.py
```
```
Enter exp: 5
Estimated Salary:  72613.84695396919
```
