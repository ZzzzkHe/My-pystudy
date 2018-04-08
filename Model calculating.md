import numpy as np
def f(v):
    a0,a1=v
    return [xy-a1*xx-a0*sigx,sigy-a1*sigx-len(x)*a0]
data=np.loadtxt(r"D:\学习相关\python计算机思维与计算求解\双曲线模型-收入-失业率.txt")

y=data[:,0]
x=data[:,1]
x=1.0/x

xy=np.sum(x*y)
xx=np.sum(x**2)
sigx=np.sum(x)
sigy=np.sum(y)

from scipy.optimize import fsolve
ans = fsolve(f, [1.0,1.0])
print (ans)
print (f(ans))

4.2	6.8
3.5	5.5
3.4	5.5
3	  6.7
3.4	5.5
2.8	5.7
2.8	5.2
3.6	4.5
4.3	3.8
5	  3.8
6.1	3.6
6.7	3.5
There are the data above.
