# Implementation of Univariate Linear Regression

## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm:

1. Start 
2. Get the independent variable X and dependent variable Y. 
3. Calculate the mean of the X -values and the mean of the Y -values. 
4. Find the slope m of the line of best fit using the formula.
 <img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
5. Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
6. Use the slope m and the y -intercept to form the equation of the line.
 
7. Obtain the straight line equation Y=mX+b and plot the scatterplot.
8. End


## Program:
```
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: JAYADEV PALLINTI
RegisterNumber: 212223240058

import numpy as np
import matplotlib.pyplot as plt

#processing input data
X=np.array(eval(input()))
Y=np.array(eval(input()))

#mean
X_mean=np.mean(X)
Y_mean=np.mean(Y)

num=0  #for slope
denom=0  #for slope

#to find sum of (xi-x') & (yi-y') & (xi-x')^2
for i in range(len(X)):
    num+=(X[i]-X_mean)*(Y[i]-Y_mean)
    denom+=(X[i]-X_mean)**2

#calculate slope
m=num/denom

#calculate intercept
b=Y_mean-m*X_mean

print(m,b)

#line equation
Y_predicted=m*X+b
print(Y_predicted)

#to plot graph
plt.scatter(X,Y)
plt.plot(X,Y_predicted,color='red')
plt.show()
```

## Output:
## slope and y-intercept
6.49131274131274 33.76833976833977

## Y predicted
[72.71621622 98.68146718 46.75096525 59.73359073 72.71621622 79.20752896
 33.76833977 40.25965251 85.6988417  66.22490347 53.24227799]

## Graph:

![Screenshot 2024-08-23 104618](https://github.com/user-attachments/assets/e9dae277-b45e-4496-a4e9-d5af51aa1586)



## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
