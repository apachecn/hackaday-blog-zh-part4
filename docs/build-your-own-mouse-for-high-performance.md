# 打造您自己的高性能鼠标

> 原文：<https://hackaday.com/2020/03/12/build-your-own-mouse-for-high-performance/>

对于专业游戏玩家或铁杆电脑用户来说，高端输入外设有很多选择。我们也看到很多制造商打造自己的定制键盘。不太常见的是定制鼠标，但[~~gipetto~~TranquilTempest]已经制作了这样一种设备来满足他们的口味。

该鼠标基于 PMW3360 传感器，因其每秒 250 英寸的速度和 50g 的加速能力而闻名。按钮由 ATMEGA32U4 读取，atmega 32 u 4 处理硬件去抖动以改善控制。任何偶然双击他们在 AOE II 的所有村民的人都可以欣赏这个特性。还有专门的代码来读取[Ben Buxton]的车轮编码器，这有助于避免回卷。

PCB 是使用他们的组装服务从 JLCPCB 订购的，这对于那些想要构建高级设计而不需要重新焊接的制造商来说很方便。它被设计成适合放在过去几年流行的微软鼠标外壳中——像滚轮鼠标光学和智能鼠标 1.3。

从头开始制作你自己的鼠标是一个很好的方法，可以让你的输入设备完全满足你的需求。我们已经看到其他人在这个领域工作，使用[定制轨迹球](https://hackaday.com/2018/06/23/roll-your-own-trackball-mouse/)和[传感器分线板。](https://hackaday.com/2016/11/21/diy-optical-sensor-breakout-board-makes-diy-optical-mouse/)如果你有自己的尖端身材，[一定要让我们知道！](http://hackaday.com/submit-a-tip)