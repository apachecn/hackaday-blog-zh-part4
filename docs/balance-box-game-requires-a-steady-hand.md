# 平衡盒游戏需要稳定的手

> 原文：<https://hackaday.com/2019/10/17/balance-box-game-requires-a-steady-hand/>

在遥远的过去，工程师们使用奇异的设备来测量方向，如大型机械陀螺仪和水银倾斜开关。这些仍然是有用的方法，但对于许多应用来说，MEMS 运动器件已经成为金标准。当[g199]着手打造他们的平衡盒游戏时，它也不例外。

这个游戏由一个塑料盒子组成，盒子上装有一个水平仪，还有一系列发光二极管。游戏的目的是保持箱子水平，同时将它带到设定的目标。在内部，Arduino Uno 监控 MPU 6050 的输出，MPU 6050 是一个结合了加速度计和陀螺仪的芯片。如果 Arduino 检测到盒子倾斜，它会用 led 警告用户。倾斜得太厉害，一条命就没了。三条命都没了，游戏也就结束了。

这是一个便宜而简单的建筑，仅仅在 10 到 20 年前会非常昂贵。它展示了 MEMS 传感器等无处不在的廉价电子产品所带来的应用。这项技术还有其他有趣的应用——[例如 Stecchino 游戏](https://hackaday.com/2018/03/23/stecchino-game-is-all-about-balancing-a-big-toothpick/)、[或者这个巨大的平衡板操纵杆。](https://hackaday.com/2016/02/06/balancing-d-pad-gets-you-in-the-game/)我们很幸运能够拥有如此强大的技术！