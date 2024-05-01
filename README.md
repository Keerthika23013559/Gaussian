# Gaussian Elimination
NAME: KEERTHIKA M P
REF.NO: 212223240071

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Import the numpy and sys module to use the built-in function for calculation.
2. Get the input input matrix.
3. With for loop do the required calculations.
4. End the program.

## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: KEERTHIKA M P
RegisterNumber:212223240071
*/
import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        a[i][j] = float(input())
for i in range(n):
    if a[i][i] == 0.0:
        sys.exit('Divide by zero detected!')
        
    for j in range(i+1,n):
        ratio=a[j][i]/a[i][i]
        
        for k in range(n+1):
            a[j][k] = a[j][k] - ratio * a[i][k]
x[n-1] = a[n-1][n]/a[n-1][n-1]

for i in range(n-2,-1,-1):
    x[i] = a[i][n]
    
    for j in range(i+1, n):
        x[i] = x[i]-a[i][j]*x[j]
        
    x[i] = x[i]/a[i][i]
for i in range(n):
    print('X%d = %0.2f' %(i,x[i]), end=' ')
```

## Output:


![Screenshot 2024-05-01 143337](https://github.com/SaiVishal1105/Gaussian/assets/162658262/09020275-eae2-4eee-80e3-80f296ff36e8)

## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

