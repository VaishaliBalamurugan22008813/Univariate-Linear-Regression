# Implementation of Univariate Linear Regression
## Aim:
To implement univariate Linear Regression to fit a straight line using least squares.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Get the independent variable X and dependent variable Y.
2.	Calculate the mean of the X -values and the mean of the Y -values.
3.	Find the slope m of the line of best fit using the formula.
 ![image](https://user-images.githubusercontent.com/119390134/214600978-367b1e45-0068-4b30-8eff-bd5726a7ab49.png)
4.	Compute the y -intercept of the line by using the formula:
![image](https://user-images.githubusercontent.com/119390134/214601185-7e367eaa-f2a6-4e9a-9eca-1aefc29333d0.png) 
5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
```
#Developed by:VAISHALI BALAMURUGAN
Register No:22008813

import numpy as np
import matplotlib.pyplot as plt
X = np.array(eval(input()))
Y = np.array(eval(input()))
Xmean = np.mean(X)
Ymean = np.mean(Y)
num, den = 0, 0
for i in range(len(X)):
num += (X[i]-Xmean)*(Y[i]-Ymean)
den += (X[i]-Xmean)**2
m = num/den
c = Ymean-m*Xmean
print(m, c)
Y_pred = m*X+c
print(Y_pred)
plt.scatter(X, Y)
plt.plot(X, Y_pred, color="red")
plt.show()



```
## Output
![image](https://user-images.githubusercontent.com/119390134/214601721-f657f67b-abc2-48cc-906c-ec922c94438b.png)

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
