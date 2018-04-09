import numpy as np
a=np.zeros((2,3))
b=np.ones((2,3))
c=np.eye(5,5)
d=np.random.standard_normal((5,5))
print(a,  b,   c,   d)

def fibs(n):
    ans=[0,1]
    for i in range(n-2):
        ans.append(ans[-2]+ans[-1])
    return ans
print(fibs(int(input('x='))))

