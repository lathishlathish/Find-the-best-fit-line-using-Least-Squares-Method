# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
4. Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:
```
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: LATHISH KANNA.M
RegisterNumber:212222230073 
*/
import numpy as np
import matplotlib.pyplot as plt
X = np.array([3.6,4.8,7.2,6.9,10.7,6.1,7.9,9.5,5.4])
Y = np.array([9.3,10.2,11.5,12,18.6,13.2,10.8,22.7,12.7])
X_mean=np.mean(X)
print(X_mean)
Y_mean=np.mean(Y)
print(Y_mean)
num=0
denum=0
for i in range(len(X)):
  num+=(X[i]-X_mean)*(Y[i]-Y_mean)
  denum+=(X[i]-X_mean)**2
m=num/denum

b=Y_mean - m*X_mean
print(m)
print(b)
Y_pred=m*X+b
print(Y_pred)
plt.scatter(X,Y)
plt.plot(X,Y_pred,color='red') 
plt.show() 
```

## Output:)
![image](https://github.com/lathishlathish/Find-the-best-fit-line-using-Least-Squares-Method/assets/120359170/b3c28243-8464-423f-be46-8e3f7d06117b)
![image](https://github.com/lathishlathish/Find-the-best-fit-line-using-Least-Squares-Method/assets/120359170/c2822d8a-1378-41b8-b1fe-42a9da54e14a)

## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
