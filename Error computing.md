import numpy as np
X=np.loadtxt(r"D:\学习相关\python计算机思维与计算求解\1.txt")
Y=np.loadtxt(r"D:\学习相关\python计算机思维与计算求解\1.txt")

Xt=X.T
XtX=Xt.dot(X)
inv=np.linalg.inv(XtX)
temp=inv.dot(Xt)
a=temp.dot(Y)


inv=np.linalg.inv(XtX)
temp=inv.dot(Xt)
a=temp.dot(Y)

X=np.loadtxt(r"D:\学习相关\python计算机思维与计算求解\1.txt")
Yhat=X.dot(a)

Y=np.loadtxt(r"D:\学习相关\python计算机思维与计算求解\1.txt")

error=np.abs(Y-Yhat)/Y*100
print(error)
