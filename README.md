# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Get the input
2. Loop through each row and column
3. Use nested loops to perform gaussian elimination
4. Print the result

## Program:
```
'''Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by: SRISHANTH J
RegisterNumber: 212223240160
'''
import numpy as np
n=int(input())
arr=np.zeros((n,n+1))
res=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        arr[i][j]=int(input())
for i in range(n):
    for j in range(i+1,n): 
        ratio=arr[j][i]/arr[i][i]
        for k in range(n+1):
            arr[j][k]=arr[j][k]-ratio*arr[i][k]
res[n-1]=arr[n-1][n]/arr[n-1][n-1]
for i in range(n-1,-1,-1):
    res[i]=arr[i][n]
    for j in range(i+1,n):
        res[i]=res[i]-arr[i][j]*res[j]
    res[i]=res[i]/arr[i][i]
for i in range(n):
    print("X%d = %0.2f" %(i,res[i]),end=" ")

```

## Output:
<img width="663" alt="Screenshot 2023-12-24 195007" src="https://github.com/srishanth2006/Gaussian/assets/150319470/05b1ec50-7893-4cd7-a55c-d652e7535072">

## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

