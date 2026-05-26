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
 ![eqn1](./eq1.jpg)
4.	Compute the y -intercept of the line by using the formula:
![eqn2](./eq2.jpg)  
5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program

```
#Program to implement univariate Linear Regression to fit a straight line using least squares.
#Developed by: jack wallace S
#RegisterNumber: 212225040136

import os
os.environ["OPENBLAS_NUM_THREADS"]="1"
import numpy as np
import matplotlib.pyplot as plt
x = np.array([0,1,2,3,4,5,6,7,8,9])
y = np.array([1,3,2,5,7,8,8,9,10,12])
plt.scatter(x,y)
plt.show()
xmean = np.mean(x)
ymean = np.mean(y)
num=0
den=0
for i in range(len(x)):
 num+=(x[i]-xmean)*(y[i]-ymean)
 den+=(x[i]-xmean) **2
m = num/den
b = ymean - m * xmean
print(m,b)
ypred = m * x+b
print(ypred)

plt.scatter(x, y, color='Red')
plt.plot(x,ypred, color='Blue')
plt.show()
```







## Output
</br><img width="918" height="764" alt="597909939-bde061a0-de15-4b70-8c4d-284ad72d86ff" src="https://github.com/user-attachments/assets/c33001e8-48b4-44d5-8981-1b4fcf113059" />

</br><img width="888" height="644" alt="597910059-ef31d5f5-0ecf-4992-b622-894ccd056baf" src="https://github.com/user-attachments/assets/d3956f73-18dd-41e9-bd5a-18ed572d6de7" />
</br>
</br>

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
