# test_tech_NCQ_algo1
import numpy as np
from numpy import zeros,array

def solution( N,A):
    V=zeros(N)
    for i in range(np.size(A)):
        if((A[i]>=1 )and(A[i]<=N)):
            V[A[i]-1]+=1
             
        elif (A[i]== N+1):
            max=0
            for j in range(N):
                if V[j]>max:
                    max=V[j]
            for i in range(N):
                V[i]=max
    return V
