# 微型 PCB 电动机器人正在进行它的第一次摇摆运动

> 原文：<https://hackaday.com/2021/05/30/tiny-pcb-motor-robot-is-making-its-first-wobbly-moves/>

[Carl Bugeja]已经为他的 PCB 电机工作了三年多，看起来他还没有耗尽这个项目的所有想法。他的最新发明是一个由蓝牙控制的微型机器人，由两个这样的马达组成。

这些[轴向磁通 PCB 电机](https://hackaday.com/2018/01/24/this-tiny-motor-is-built-into-a-pcb/)的一个主要挑战是它们的低扭矩输出，所以【Carl】必须尽可能地让机器人变轻。主板包含一个集成蓝牙的微控制器模块、一个 IMU、调节器和两个电机驱动器。电机定子板使用 90 个插头引脚焊接到主板上。车身的框架和马达的转子都是 3D 打印的。一组四个钕磁铁和一个轴承压配合到每个转子中。电机轴是现成的 PCB 引脚，一端焊接到定子板上。电力来自连接到主板的一个小的单节脂肪电池。

机器人移动了，但是是以一种急动的方式，并且一直在做一些意想不到的转弯。这种情况的主要原因似乎是转子不稳定，这意味着输出扭矩在电机旋转过程中波动。由于只有两个接触地面的点，只有电路板和电池的重量阻止了中心部分随电机旋转。这看起来还不够，所以[Carl]想尝试使用 IMU 来平滑运动。对于下一个版本，他还在研究新的轴架、金属转子和更高效的电机设计。

我们期待看到它的实际应用，以及[Carl]能想到的其他应用。他已经试验过把它变成一个[步进电机](https://hackaday.com/2020/12/11/microstepping-a-pcb-motor/)、[直线电机](https://hackaday.com/2018/06/11/pcbs-as-linear-motors/)和[微型拼图电机](https://hackaday.com/2019/07/16/jigsaw-motor-uses-pcb-coils-for-radial-flux/)。

 [https://www.youtube.com/embed/ezONF7bKqfs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ezONF7bKqfs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

