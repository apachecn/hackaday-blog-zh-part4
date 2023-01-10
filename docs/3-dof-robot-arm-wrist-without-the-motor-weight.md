# 无电机重量的三自由度机器人臂腕

> 原文：<https://hackaday.com/2022/11/03/3-dof-robot-arm-wrist-without-the-motor-weight/>

机械臂的一个主要挑战是致动器的重量，特别是靠近臂末端的部分。长杠杆臂意味着其他致动器需要更大的扭矩，所有部件都会弯曲得更厉害一些。为了解决这个问题， [[RoTechnic]将手腕步进电机从手臂上完全移开](https://www.youtube.com/watch?v=0hGy4AxUOnk)。

他建立了一个推拉机制，使用编织渔线通过鲍登管将运动传递到机器人手臂的手腕。马达安装在手臂的底座上，轴上有一个鼓和两根钓鱼线。这些线在进入波顿管之前会穿过一个可调节的张紧器。这种鼓机制也存在于手腕的三个旋转轴的每一个上。

[RoTechnic]使用 Arduino 供电的 RAMPS 板作为控制器，通过编程接受串行接口。他在 Jupyter Labs 中创建了一个简单的 GUI 和脚本接口来生成和发送命令，这似乎是一个优秀的测试解决方案。

我们可以看到这种机制在各种运动应用中非常有用，并且肯定会添加到 idea toolbox 中。这有点类似于我们在[人形机器人](https://hackaday.com/2019/10/20/humanoid-robot-has-joints-that-inspire/)和其他 [3D 打印手臂](https://hackaday.com/2020/04/26/cable-driven-robotic-joint/)中看到的其他一些电缆操作关节。

 [https://www.youtube.com/embed/0hGy4AxUOnk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/0hGy4AxUOnk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

