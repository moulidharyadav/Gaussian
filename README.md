# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
```
1.IMport the numpy module to use the built_in functions for calculation.
2.Import sys module to use the built_in functions.
3.Get the input from the user for number of rows and add it by 1 for number of columns.
4.Using np.zeros() set the matrix as null matrix .
5.Using nested for loop get input from the user for each element in the matrix.
6.Using nested for loop input find the ration and perform the elementary row operations and find the final matrix.
7.Use back substituion method to find the value of the variable and print it.
8.End the program.
```
## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: MOULIDHAR.G
RegisterNumber: 2300285
*/
import numpy as np
n=int(input())
arr=np.zeros((n,n+1))
x=np.zeros(n)
for  i in range(n):
    for j in range(n+1):
        arr[i][j]=int(input())
for i in range(n):
    for j in range(i+1,n):
        ratio=arr[j][i]/arr[i][i]
        for k in range(n+1):
            arr[j][k]=arr[j][k]-ratio*arr[i][k]
x[n-1]=arr[n-1][n]/arr[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=arr[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-arr[i][j]*x[j]
    x[i]=x[i]/arr[i][i]
for i in range(n):
    print("X%d = %0.2f" %(i,x[i]),end=" ")
```

## Output:
![gaussian elimination]()
![Screenshot 2023-12-25 144526](https://github.com/moulidharyadav/Gaussian/assets/147078316/3d1b93e7-7a56-483c-80f1-598c8154fdbb)



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

