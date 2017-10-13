import matplotlib.pyplot as plt
import numpy as py
import math

xa=0
ya=0
xb=0
yb=0
xc=0
yc=0
f1=[0]
z1=[0]
f2=[0]
z2=[0]
f3=[0]
z3=[0]
v=700
t=0.001 
vx1=v*math.cos(math.radians(angel1))
vy1=v*math.sin(math.radians(angel1))
vx2=v*math.cos(math.radians(angel2))
vy2=v*math.sin(math.radians(angel2))
vx3=v*math.cos(math.radians(angel3))
vy3=v*math.sin(math.radians(angel3))
a=4*10**-5
d="炮弹落点距离="

while ya>=0:
    angel1=35
    vx1=vx1-a*v*vx1*t
    vy1=vy1-9.8*t-a*v*vy1*t
    x1=xa
    y1=ya
    xa=xa+vx1*t
    ya=ya+vy1*t
    b=-y1/ya
    v=py.sqrt(vx1**2+vy1**2)
    t=t+0.001
    f1.append(xa)
    z1.append(ya)
    l1=(xa+b*x1)/(b+1)
print(d,l1) 

while yb>=0:
    angel2=45
    vx2=vx2-a*v*vx2*t
    vy2=vy2-9.8*t-a*v*vy2*t
    x2=xb
    y2=yb
    xb=xb+vx2*t
    yb=yb+vy2*t
    b=-y2/yb
    v=py.sqrt(vx2**2+vy2**2)
    t=t+0.001
    f2.append(xb)
    z2.append(yb)
    l2=(xb+b*x2)/(b+1)
print(d,l2)    

while yc>=0:
    angel2=55
    vx3=vx3-a*v*vx3*t
    vy3=vy3-9.8*t-a*v*vy3*t
    x3=xc
    y3=yc
    xc=xc+vx3*t
    yc=yc+vy3*t
    b=-y3/yc
    v=py.sqrt(vx3**2+vy3**2)
    t=t+0.0001
    f3.append(xc)
    z3.append(yc)
    l3=(xc+b*x3)/(b+1)
print(d,l3) 

plt.figure(figsize=(8,4))
plt.plot(f1,z1,label="$θ=40°$",color='blue',linewidth='1')
plt.plot(f2,z2,label="$θ=45°$",color='red',linewidth='1')
plt.plot(f3,z3,label="$θ=50°$",color='green',linewidth='1')
plt.xlabel("X/m")
plt.ylabel("Y/m")
plt.title("Canon Shell Trajectory")
plt.ylim(0,10000)
plt.legend()
plt.show()
