import numpy as np
class MLR:
    def __init__(self,x,y):
        self.x=x
        self.y=y
    def modelling(self):
        oneCol=np.ones(self.x.shape[0])
        X=np.c_[oneCol,self.x]
        Xt=X.T
        XtX=Xt.dot(X)
        inv = np.linalg.inv(XtX)
        temp =inv.dot(Xt)
        self.a=temp.dot(self.y)
    def predict(self,xnew):
        oneCol=np.ones(xnew.shape[0])
        x=np.c_[oneCol,xnew]
        ynew=x.dot(self.a)
        return ynew
