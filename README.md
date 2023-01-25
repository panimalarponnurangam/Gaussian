# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. In this experiment we importinr numpy as np and getting three input values.
2. Then we using loop and nested loop for find out matrix
3.Then we assigning the values for variable in the loop 
4.Finally printing the output. 

## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: panimalar.p
RegisterNumber: 22009107
*/
import numpy as np
import sys
n= int(input())
a=np.zeros((n,n+1))
X=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        a[i][j] = float(input())
for i in range(n):
    if a[i][j] == 0.0:
       sys.exit("Divide by zero detected!")
    for j in range(i+1, n):
        ratio = a[j][i]/a[i][i]
        for k in range(n+1):
            a[j][k] = a[j][k] - ratio * a[i][k]
X[n-1] = a[n-1][n]/a[n-1][n-1]
for i in range (n-2,-1,-1):
    X[i] = a[i][n]
    for j in range(i+1,n):
        X[i] = X[i] -a[i][j]*X[j]
    X[i] = X[i]/a[i][i]
for i in range(n):
    print("X%d = %0.2f" %(i,X[i]) , end = " ")

```

## Output:

![Screenshot (176)](https://user-images.githubusercontent.com/121490826/214635863-e628e100-11be-421b-96a7-a1d25139c7d6.png)


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

