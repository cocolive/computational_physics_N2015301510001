# 摘要：
 用欧拉法解常微分方程初值问题

# 题目
It is often the case that the frictional force on an object will increase as the object moves faster. A fortunate example of this is a parachutist; the role of the parachute is to produce a frictional force due to air drag , which is larger than would normally be the case without the parachute. The physics of air drag will be discussed in more detail in the next chapter. Here we consider a very simple example in which the frictional force depends on the velocity. Assume that the velocity of an object obeys an equation of the form where a and b are constants. You could think of a as coming from an applied force such as gravity, while arises from friction. Note that the frictional force is negative（we assume that b > 0 ), so that it opposes the motion, and that it increases in magnitude as the velocity increases. Use the Euler method to solve the equation for v as a function of time.

#                                                   ![](https://github.com/cocolive/compuational_physics_N2015301510001/blob/master/%E4%BD%9C%E4%B8%9A3.1.png)
                     

 # 解题思路
 - 函数库：matplotlib
 - 所需对应语句： form pylab import
 - 具体计算方法：数值计算法、欧拉法近似求解
 - 时间间隔dt选取得越短，则模拟计算越精确
 
 # 欧拉法分析:
 ## #                      ![](https://github.com/cocolive/compuational_physics_N2015301510001/blob/master/3.2.gif)
 保留一阶项：               
 ##          #                              ![](https://github.com/cocolive/compuational_physics_N2015301510001/blob/master/3.3.gif)
 联立微分方程可得：   
 ## #                         ![](https://github.com/cocolive/compuational_physics_N2015301510001/blob/master/3.4.gif)
 
 # 解题成果
 [代码链接](https://github.com/cocolive/computational_physics_N2015301510001/blob/master/Code_03) 
  
  取a=10，b=1
  运行图像：
  
  - 初速度为0：
   
   ![](https://github.com/cocolive/compuational_physics_N2015301510001/blob/master/yOo%2B1R44r%2BbAAAAAElFTkSuQmCC.png)  
 
  - 初速度为20m/s:
  
   ![](https://github.com/cocolive/compuational_physics_N2015301510001/blob/master/DwG2EK%2BfWj6hAAAAAElFTkSuQmCC.png)
    
 # 结论：
   降落伞模型中，如果速度低于![](https://github.com/cocolive/compuational_physics_N2015301510001/blob/master/CodeCogsEqn.gif),此时重力大于阻力，速度会增加，速度增加后，同时会伴随着阻力增大，此时合力变小，加速度减小，但方向仍竖直向下，所以图像上斜率逐渐变小，速度一直增加到改大小后，此时重力等于阻力，合力为0，加速度为0，速度保持恒定，匀速下降；同样如果速度大于v,此时重力小于阻力，速度会降低，速度减小后，同时会伴随着阻力减小，此时合力变小，加速度减小，但方向仍竖直向上，保持减速，所以图像上斜率逐渐变小，直到速度减小为v，此时重力等于阻力，速度保持恒定，匀速下降；匀速运动时的速度大小只取决于a、b。
 
