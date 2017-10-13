 import matplotlib.pyplot as plt
 import numpy as py
 import math
 

 f=[0]
 z=[0]
 v=float(input("请输入初始速度："))
 t=0.00001 
 angel=float(input("请输入初射角度："))
 vx=v*math.cos(math.radians(angel))
 vy=v*math.sin(math.radians(angel))
 a=4*10**-5
 d="炮弹落点距离="
 for i in range(100):
         angel=angel+0.05
         x=0
         y=0
         while y>=0:
             vx=vx-a*v*vx*t
             vy=vy-9.8*t-a*v*vy*t
             x1=x
             y1=y
             x=x+vx*t
             y=y+vy*t
             b=-y1/y
             v=py.sqrt(vx**2+vy**2)
             t=t+0.00001
             l=(x+b*x1)/(b+1)
         print(angel,l)
 plt.figure(figsize=(8,4))
 plt.plot(l,angel,marker='.')
 plt.xlabel("θ/°")
 plt.ylabel("l/m")
 plt.title("Canon Shell Trajectory")
 plt.ylim(0,10000)
 plt.legend()
 plt.show()
