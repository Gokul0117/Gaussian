# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm

1.Import numpy from the Python libraray. 

2.Get the matrix input from the user. 

3.Calculate the variable using libraries. 

4.Print the result.

5.End the Program

 

## Program:
```

Program to find the solution of a matrix using Gaussian Elimination.
Developed by:Gokul J 
RegisterNumber:22009062 
import numpy as np
n=int(input())
arr=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
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
![gaussian elimination](https://user-images.githubusercontent.com/121165938/214586702-ce4d9a7b-4b42-420e-b370-3324f6652366.png)



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

