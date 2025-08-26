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

x = np.array ([3.6,4.8,7.2,6.9, 10.7,6.1,7.9,9.5,5.4])

y = np.array ([9.3,10.2,11.5,12,18.6,13.2,10.8,22.7,12.7])

ypred = 1.53*x+2.88

print("x values:")

print(x)

print("y values: ")

print(y)

plt.scatter(x,y,color='Black')

plt.plot(x,ypred, color='Red')

plt.show()

```

## Output:

<img width="909" height="675" alt="Screenshot 2025-08-26 153911" src="https://github.com/user-attachments/assets/a5c7c33b-b6ca-4d2e-bd6f-11742d65f26c" />

## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
