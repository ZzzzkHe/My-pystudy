import numpy as np
a=np.array([[1,2,3],[4,5,6]])
b=np.ones(3)
c=np.insert(a,2,b,axis=0)
print(c)
b=np.ones(2)
c=np.c_[b,a]
print(c)

Data=np.loadtxt (r"D:\学习相关\python计算机思维与计算求解\一元线性回归数据.txt")
X=Data[:,0]
Y=Data[:,1]
oneCol=np.ones(X.shape[0])
X=np.c_[oneCol,X] 
Xt=X.T
XtX=Xt.dot(X)
inv=np.linalg.inv(XtX)
temp=inv.dot(Xt)
a=temp.dot(Y)
print(a.round(6))

4.13    9.585010958
8.51    19.21960826
0.93    2.53595872
8.69    19.61827865
7.31    16.57609295
5.49    12.58636965
0.60    1.828331933
2.03    4.96526275
7.87    17.815749
1.94    4.771571055

Here are the data above.
