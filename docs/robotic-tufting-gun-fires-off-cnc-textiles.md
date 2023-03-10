# 机器人簇绒枪发射数控纺织品

> 原文：<https://hackaday.com/2022/03/05/robotic-tufting-gun-fires-off-cnc-textiles/>

簇绒通常用于制作地毯，是一种使用空心针将线或纱线以某种图案塞入织物的工艺。这可以用手、枪或大型机器来完成。一些机器被设置成一遍又一遍地快速冲压相同的图案，而这些机器很难为新的图案重新装备。其他人被制造成戳任意的模式并且容易改变，但是这些机器移动得更慢。

[![](img/789d3940288349d49ff96fcbc821b953.png)](https://hackaday.com/wp-content/uploads/2022/03/tufting-gun.gif) 这个[由【欧文·特鲁布拉德】开发的机器人簇绒系统](https://hackaday.io/project/184058-robotic-tufting-system)属于缓慢而随意的类型。它将由一个经过改造的簇绒枪组成，该簇绒枪系在用于 CNC 纺织艺术的机器人手臂上。簇绒枪的制造具有简单的控制装置——一个电源开关、一个设置速度的旋钮和一个启动按钮来进行簇绒。一旦它被固定在机器人手臂上，[欧文]想要遥控它。

枪的电机驱动器没有什么花哨的，只是一个 555 使用 PWM 控制半 H 桥的基础上输入速度控制电位器。[Owen]用 Arduino 替换了电机控制器并增加了一个 I/O 端口。后者是一个 3.5 毫米立体声音频插孔，连接到 GND 和 Arduino 的两个引脚。一个是为枪供电的数字输入，另一个用作基于输入电压的模拟速度控制器。[欧文]才刚刚开始，我们很高兴能继续关注这个项目，因为枪变成了机器人。

这并不是我们第一次看到机器人做纺织品——这是一个编织碳纤维的 6 轴机械臂。