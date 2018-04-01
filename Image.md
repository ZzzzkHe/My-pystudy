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
plot(Y,X,color='pink')
show() #heartflow in rectangular coordinates

m=np.linspace(0,8*np.pi,1314)
a=(1+2*m)*np.cos(m)
b=(1+2*m)*np.sin(m)
plot(b,a,color='red')
show() #This one may be better. Why? Love is always endless.
