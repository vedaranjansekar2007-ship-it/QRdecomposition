# Algorithm for QR Decomposition
## Aim:
To implement QR decomposition algorithm using the Gram-Schmidt method.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:




## Program:
### Gram-Schmidt Method
```

import numpy as np
def qr_decomposition(A):
    A=np.array(A,dtype=float)
    m,n=A.shape
    Q=np.zeros((m,n))
    R=np.zeros((n,m))
    for j in range(n):
        v=A[:,j]
        for i in range(j):
            R[i,j]=np.dot(Q[:,i],A[:,j])
            v=v-R[i,j]*Q[:,i]
        R[j,j]=np.linalg.norm(v)
        Q[:,j]=v/R[j,j]
    return Q,R
A=np.array(eval(input()))
Q,R=qr_decomposition(A)
print("The Q Matrix is\n",Q)
print("The R Matrix is\n",R) 

```

## Output
```
<img width="1920" height="1020" alt="Screenshot 2025-12-10 202650" src="https://github.com/user-attachments/assets/c8f3b47a-eabc-4a50-b9b4-b726778ec7cd" />

```

## Result
Thus the QR decomposition algorithm using the Gram-Schmidt process is written and verified the result.
