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
import numpy as np
import matplotlib.pyplot as plt

# Using sample data directly for demonstration
x = np.array([1, 2, 3, 4, 5])
y = np.array([2, 4, 5, 4, 5])

x_mean = np.mean(x)
y_mean = np.mean(y)

num, den = 0, 0
for i in range(len(x)):
  num += ((x[i] - x_mean) * (y[i] - y_mean))
  den += ((x[i] - x_mean)**2)

# Handle the case where den is zero to avoid division by zero
if den == 0:
    m = 0
    b = y_mean
else:
    m = num / den
    b = y_mean - m * x_mean

print("Slope:", m)
print("Intercept:", b)

y_predit = m * x + b
print("Predicted y values:", y_predit)

plt.scatter(x, y, color='yellow')
plt.plot(x, y_predit, color='red')
plt.title("Linear Regression with Sample Data")
plt.xlabel("x")
plt.ylabel("y")
plt.show()

```

## Output:

<img width="715" height="650" alt="image" src="https://github.com/user-attachments/assets/c38d0c0a-2ad2-4ceb-8768-164643723de3" />

## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
