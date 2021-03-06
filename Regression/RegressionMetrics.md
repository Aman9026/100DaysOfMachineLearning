# Regression

Regression is a task when model attempts to predict continuous values

## Ordinary Least Square method:
Regression algorithm is trying to find best fitting line, by minimize the square of sum of all predicted and actual value 
```
Sum of Square of Residual = SUM( y - y^)2 
```
## R Squared:
```
SSres = SUM(y - y^)2
SStot = SUM(y-Yavg)2

R2 = 1 - SSres/SStot
```
**Where:** Yavg, is average line of all data points, y is actual value, y^ is predicted value

If R2 = 1, that is ideal scenario, when SSres = 0,

Means R2 if more close to 1, then model is better


## Adjusted R square:
If we add some more variable in function, R squared dont change, so harder to find, 
How this variable affecting model, so this is the problem in **R square**, that why we can use **Adjusted R square**

Adjusted R square, use **penalize method**, it penalize model, if we add more variable, that don’t help model
```
Adj R2 = 1 - ( 1 - R2) n-1/ n-p-1
```
Where: p = number of regressors
	 n = sample size



## Evaluation Metrics for regression: 
All of these are loss function, so we have to minimize them

* Mean Absolute Error - **MAE**
* Mean Squared Error - **MSE**
* Root Mean Square Error - **RMSE**

### MAE
![](https://github.com/Aman9026/100DaysOfMachineLearning/blob/master/Data/Images/MAE.png)

MAE won’t punish large errors, so we use MSE, means larger error are noted more than with MAE, making MSE more popular

### MSE 
![](https://github.com/Aman9026/100DaysOfMachineLearning/blob/master/Data/Images/MSE.png)

### RMSE: most popular 
![](https://github.com/Aman9026/100DaysOfMachineLearning/blob/master/Data/Images/RMS.png)

Domain Knowledge also plays an important role
![](https://github.com/Aman9026/100DaysOfMachineLearning/blob/master/Data/Images/samplegraph3.png)

Our goal with linear regression is to minimize the vertical distance between all the data points and our line and determining the best fit line
We will use the Least Square Method, which is fitted by minimizing the sum of squares of the residuals

### Residual 
It is the difference between the observation (y value) to fitted line or predicted value (y hat)

