# TrueTape64 是用于 C64 数据集的 PC 接口

> 原文：<https://hackaday.com/2021/05/10/truetape64-is-a-pc-interface-for-your-c64-datasette/>

追溯到遥远的 20 世纪 80 年代，软件是通过录音带发行的。“1”和“0”被编码成不同频率的音调，磁带由专门的硬件解码，然后将原始数字数据传送到相连的计算机。虽然现在有软件方法可以简单地从旧磁带上录制音频并将其转换成数据，但[Francesco]想用硬件的方式来做这件事，[并为他的 Commodore 64 Datasette 建立了一个 PC 界面。](https://github.com/francescovannini/truetape64)

TrueTape64，正如它的名字一样，是围绕 Atmel ATTiny2313 微控制器构建的。这与原始数据集硬件接口，该硬件负责读取模拟磁带输出并将其转换为数字数据。从那里，微控制器与 FTDI232 串行转 USB 适配器通信，将数据传输到现代 PC，在那里通过一些 Python 魔术将数据编译成 TAP 图像文件。

这是一个准系统，它甚至可以通过升压转换器从 USB 电源上运行 Datasette 的电机；那些面临磁带机制问题的人最好先看看那里。然而，它确实起作用了，而且一天结束时，一个完成的工作就是一个好工作。[我们以前也见过类似的黑客攻击](https://hackaday.com/2020/11/10/proper-cassettes-for-your-fpga-retrocomputer/)——很高兴看到社区保持卡式软件的活力！