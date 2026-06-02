# MAI_EXP-6
# EXP-6 Gaussian Elimination
## Name: POOJA PRIYA B
## RegisterNumber: 212224230196

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
Step 1: 
        Start

 Step 2: 
        Read the number of variables n.

Step 3: 
        Read the augmented matrix A of size n × (n+1).

Step 4: 
        Perform Forward Elimination

## Program:
```
'''Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by: KIRUTHIKA N
RegisterNumber: 212224230127
'''
import os
os.environ["OPENBLAS_NUM_THREADS"]="1"
import numpy as np  
n=int(input())
a,b=[],[]
for i in range(n):
    t=[]
    for j in range(n):
        t.append(int(input()))
    a.append(t)    
    b.append(int(input()))
n=len(b)
x=[0]*n
for k in range(n):
    for i in range(k+1,n):
        factor=a[i][k]/a[k][k]
        for j in range(k,n):
            a[i][j]=a[i][j]-factor*a[k][j]
        b[i]=b[i]-factor*b[k]
    for i in range(n-1,-1,-1):
        sum_ax=0
        for j in range(i+1,n):
            sum_ax+=a[i][j]*x[j]
        x[i]=(b[i]-sum_ax)/a[i][i]
for i in range(len(x)):
    print(f"X{i} = {x[i]:.2f}",end=" ")
```

## Output:
<img width="1263" height="603" alt="6" src="https://github.com/user-attachments/assets/908db800-be41-485a-801b-c2b4e6f49074" />


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.
