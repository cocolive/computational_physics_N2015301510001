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
# #                      ![](https://github.com/cocolive/compuational_physics_N2015301510001/blob/master/3.2.gif)
 保留一阶项：               
 ##  #                             ![](https://github.com/cocolive/compuational_physics_N2015301510001/blob/master/3.3.gif)
 联立微分方程可得：   
 ##  #                         ![](https://github.com/cocolive/compuational_physics_N2015301510001/blob/master/3.4.gif)
 
 # 解题成果
 [代码链接]() 
  
  运行图像：
 
