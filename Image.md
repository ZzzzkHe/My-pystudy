import numpy as np #simplify the representation of numpy
from pylab import* #import pylab which is close to matlab  '*' means all except files begun with _
x=np.linspace(-np.pi,np.pi,1000) #produce a series of homogeneous linear vectors between x1 and x2
sin,cos=np.sin(x),np.cos(x) #simplify
plot(x,sin,color='blue',linewidth=2.0,linestyle='-')
plot(x,cos,color='green',linewidth=2.0,linestyle='-.')
show()

t=np.linspace(0,2*np.pi,1024)
axes(polar=True)
plot(t,1.-np.sin(t),color='pink')
show() #heartflow in polar coordinates

T=np.linspace(0,2*np.pi,520)
X=(2*np.cos(T)-np.cos(2*T))
Y=(2*np.sin(T)-np.sin(2*T))
plot(Y,X,color='pink',label='love')
xlabel('弧度')
ylabel('daddy')
title('0.0')
grid(True)
legend(loc='upper right')
show() #heartflow in rectangular coordinates

m=np.linspace(0,8*np.pi,1314)
a=(1+2*m)*np.cos(m)
b=(1+2*m)*np.sin(m)
plot(b,a,color='red')
grid(True)
show() #This one may be better. Why? Love is always endless.

data=np.random.randint(1,11,5)
pie(data,explode=[0,0,-0.3,0,0])

from sklearn import datasets
iris=datasets.load_iris()
X=iris.data
y=iris.target
z1=y==0
plot(X[z1,0],X[z1,1],'ro')
z1=y==1
plot(X[z1,1],X[z1,2],'ko')
show()
