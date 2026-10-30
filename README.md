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
Developed by: THULASI J
RegisterNumber: 212224250020
*/
import numpy as np
import matplotlib.pyplot as plt

# Get independent and dependent variables
X = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10])
Y = np.array([0, 3, 5, 7, 9, 11, 13, 2, 4, 8])

# Calculate mean values
mean_X = np.mean(X)
mean_Y = np.mean(Y)

# Calculate slope
m = np.sum((X - mean_X) * (Y - mean_Y)) / np.sum((X - mean_X)**2)

# Calculate y-intercept
b = mean_Y - m * mean_X

# Calculate predicted Y values
Y_pred = m * X + b

# Display the regression equation
print("Slope (m) =", m)
print("Y-intercept (b) =", b)
print("Regression Equation: Y =", m, "X +", b)

# Plot scatterplot and regression line
plt.scatter(X, Y, color='blue', label='Actual Data')
plt.plot(X, Y_pred, color='red', label='Best Fit Line')

plt.xlabel("Independent Variable (X)")
plt.ylabel("Dependent Variable (Y)")
plt.title("Univariate Linear Regression")
plt.legend()
plt.grid(True)
plt.show()


```



## Output:
<img width="675" height="579" alt="image" src="https://github.com/user-attachments/assets/c6fb2942-afd0-4ce3-8579-9a9c423dfe4a" />


## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
