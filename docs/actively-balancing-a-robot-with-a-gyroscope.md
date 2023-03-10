# 用陀螺仪主动平衡机器人

> 原文：<https://hackaday.com/2021/05/17/actively-balancing-a-robot-with-a-gyroscope/>

自平衡机器人是一个常见的黑客项目，但我们并不经常看到他们使用旋转陀螺仪来实现这种平衡。机器人大师[詹姆斯·布鲁顿]决定从一个简单的[概念验证](https://www.youtube.com/watch?v=UVJx8T8wTQA)开始，建造一个具有[主动陀螺稳定](https://www.youtube.com/watch?v=drxzs0Dnz14)的机器人平台。

陀螺仪可以平衡，但不能主动直接抵消外力。然而，如果陀螺仪围绕一个轴倾斜，它将施加一个垂直于倾斜轴的力，这就是所谓的陀螺进动。通过用致动器倾斜陀螺仪，并且正确地定向陀螺仪，陀螺仪进动可以用于稳定。这就是所谓的控制力矩陀螺仪。[James]通过 3D 打印的概念证明演示了这一点，它被用作 IMU 来测量倾斜角，并使用 PID 环路来校正不平衡，伺服驱动陀螺仪。

他的第二个平台使用一对旋转方向相反的陀螺仪来补偿沿另一个轴的任何意外回转进动。一对滚轴溜冰鞋轮子允许整个平台向前滚动。由于平台的轻微不平衡，[詹姆斯]注意到陀螺仪将继续向一个方向爬行，直到到达终点并翻倒。通过添加第二个软件控制器来跟踪陀螺仪必须移动多少才能保持平衡，它可以不断计算和更新平衡点。这可以防止陀螺仪碰到终点挡板。

控制力矩陀螺仪通常用于航天器的姿态控制，以及减少船只在波浪中的摇摆运动。[James]计划将控制力矩陀螺仪与更传统的平衡方法结合起来，在一个轮子上平衡机器人。

我们以前见过[两轮遥控汽车](https://hackaday.com/2019/09/06/who-needs-four-wheels-when-youve-got-a-gyro/)使用[陀螺仪](https://hackaday.com/2014/05/08/two-wheeler-is-gyroscope-stabilized/)，但是没有主动控制部分。

 [https://www.youtube.com/embed/drxzs0Dnz14?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/drxzs0Dnz14?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/UVJx8T8wTQA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/UVJx8T8wTQA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

