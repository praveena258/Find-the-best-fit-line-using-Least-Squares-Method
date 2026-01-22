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
Developed by: PRAVEENA D
RegisterNumber:  212224040248
*/

import matplotlib.pyplot as plt


X = [1, 2, 3, 4, 5]
Y = [2, 4, 5, 4, 5]

n = len(X)

mean_X = sum(X) / n
mean_Y = sum(Y) / n

num = 0
den = 0
for i in range(n):
    num += (X[i] - mean_X) * (Y[i] - mean_Y)
    den += (X[i] - mean_X) ** 2

m = num / den

b = mean_Y - m * mean_X

print("Mean of X:", mean_X)
print("Mean of Y:", mean_Y)
print("Slope (m):", m)
print("Intercept (b):", b)
print("Equation: Y =", m, "* X +", b)
plt.scatter(X, Y)
plt.plot(X, [m*x + b for x in X])
plt.xlabel("X")
plt.ylabel("Y")
plt.title("Line of Best Fit")
plt.show()

```

## Output:

<img width="567" height="453" alt="download" src="https://github.com/user-attachments/assets/d69962e7-6e61-4b4a-b59a-42b2fc8c8df8" />


## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
