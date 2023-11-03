# Correlation and regression for data analysis
# Aim : 

To analyse given data using coeffificient of correlation and regression line
![image](https://user-images.githubusercontent.com/104613195/168224136-d6b64e64-7d3d-4775-9337-c8f96fe41f2d.png)


# Software required :  

Python

# Theory:

Correlation describes the strength of an association between two variables, and is completely symmetrical, the correlation between A and B is the same as the correlation between B and A. However, if the two variables are related it means that when one changes by a certain amount the other changes on an average by a certain amount.  

If y represents the dependent variable and x the independent variable, this relationship is described as the regression of y on x. The relationship can be represented by a simple equation called the regression equation. The regression equation representing how much y changes with any given change of x can be used to construct a regression line on a scatter diagram, and in the simplest case this is assumed to be a straight line.

# Procedure :

![image](https://user-images.githubusercontent.com/104613195/168225866-ac8f6610-bdc3-4ac2-a24e-2b24ba08e189.png)

# Program :

Name:Jivan Karthec.B.S

Regno:212222100017

```python
import numpy as np
import math
import matplotlib.pyplot as plt
x=[ int(i) for i in input().split()]
y=[ int(i) for i in input().split()]
N=len(x)
Sx=0
Sy=0
Sxy=0
Sx2=0
Sy2=0
for i in range(0,N):
    Sx=Sx+x[i]
    Sy=Sy+y[i]
    Sxy=Sxy+x[i]*y[i]
    Sx2=Sx2+x[i]**2
    Sy2=Sy2+y[i]**2
r=(N*Sxy-Sx*Sy)/(math.sqrt(N*Sx2-Sx**2)*math.sqrt(N*Sy2-Sy**2))
print("The Correlation coefficient is %0.3f"%r)
byx=(N*Sxy-Sx*Sy)/(N*Sx2-Sx**2)
xmean=Sx/N
ymean=Sy/N
print("The Regression line Y on X is ::: y = %0.3f + %0.3f (x-%0.3f)"%(ymean,byx,xmean))
plt.scatter(x,y)
def Reg(x):
  return ymean + byx*(x-xmean)
x=np.linspace(20,80,51)
y1=Reg(x)
plt.plot(x,y1,'r')
plt.xlabel('x-data')
plt.ylabel('y-data')
plt.legend(['Regression Line','Data points'])
```

# Output :

<img width="392" alt="278967922-29df05b5-2a32-4508-bb1c-da0c29c409da" src="https://github.com/JivanKarthick/Correlation_Regression/assets/121165867/a91941b2-64e1-4130-a7a4-53b79f8ad21f">


# Result:
The Correlation and regression for data analysis of objects from feeder using probability distribution are calculated.
