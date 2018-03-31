import numpy as np #simplify the representation of numpy
import pylab as lab#import pylab which is close to matlab  '*' means all except files begun with _
x=np.linspace(-np.pi,np.pi,1000)#produce a series of homogeneous linear vectors between x1 and x2
sin,cos,pi=np.sin(x),np.cos(x),np.pi#simplify
lab.plot(x,sin,color='blue',linewidth=2.0,linestyle='-')
lab.plot(x,cos,color='green',linewidth=2.0,linestyle='-.')
lab.show()

t=np.linspace(0,2*pi,1024)
lab.axes(polar=True)
lab.plot(t,1.-sin(t),color='pink')
lab.show() #heartflow in polar coordinates

T=np.linspace(0,2*pi,1024)
X=(2*cos(T)-cos(2*T))
Y=(2*sin(T)-sin(2*T))
lab.plot(Y,X,color='pink')
lab.show() #heartflow in rectangular coordinates

m=np.linspace(0,2*pi,520)
a=(2*cos(m)-cos(2*m))*m
b=(2*sin(m)-sin(2*m))*m
lab.plot(b,a,color='red')
lab.show()
