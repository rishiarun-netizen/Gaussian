# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1.Input matrix dimensions and initialize augmented matrix and solution vector.

2.Populate the augmented matrix with user inputs.

3.Perform Gaussian elimination to reduce the matrix to upper triangular form, ensuring no division by zero.

4.Back substitute to compute solution values for the variables.

5.Print the solution vector formatted to two decimal places.


## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: Rishi Arun.S 
RegisterNumber: 26013829
import os
os.environ["OPENBLAS_NUM_THREADS"]="1"
import numpy as np
n = int(input())
a = np.array([float(input()) for i in range(n*(n+1))]).reshape(n,n+1)

for i in range(n):
    for j in range(i+1,n):
        r = a[j][i]/a[i][i]
        a[j] = a[j] - r*a[i]
x = np.zeros(n)

for i in range(n-1,-1,-1):
    x[i] = (a[i][n] - sum(a[i][j]*x[j]
for j in range(i+1,n))) / a[i][i]

for i in range(n):
    print(f"X{i} = {x[i]:.2f}",end=" ")

*/
```

## Output:
![gaussian elimination]()
<img width="512" height="230" alt="Screenshot 2026-11-27 213759" src="https://github.com/user-attachments/assets/eb1384ba-1d58-4546-a0ae-688a2804c7f4" />



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

