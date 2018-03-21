# My-pystudy
A start of my pystudy，
import math
print("请输入自变量为x的高次python表达式！")
print("例如：x**5-4.7*x**4-3.7*x**3+1.8*x**2+23.8*x-120.4")
equ=input("equ=")
while True:
    a=float(input("input a:"))
    b=float(input("input b:"))
    x=a;   fa=eval(equ)
    x=b;   fb=eval(equ)
    if(fa*fb<1e-12):
        break
while abs((b-a)/a)>1e-6:
    m=(a+b)/2
    x=m
    fm=eval(equ)
    if fm*fb>0:
        b=m
    else:
        a=m
print(a)
x=a
print(eval(equ))
