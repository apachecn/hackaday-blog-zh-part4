# 用 Nixies 制作 20 世纪 40 年代的数字收音机

> 原文：<https://hackaday.com/2019/03/17/making-a-1940s-radio-digital-with-nixies/>

费城 1079 号是你的费城灵魂之家，就在表盘的顶端。“表盘顶端”这句话现在已经没什么意义了，因为我们都有带数字显示和搜索按钮的收音机。曾几何时，收音机实际上是有刻度盘的，但[格拉斯林格]是独一无二的。他正在给一台 20 世纪 40 年代的收音机增加一个数字显示器，他正在用谢妮电子管做这件事。

该调幅收音机的数字显示电路需要获得收音机调谐到的频率。这是通过计算振荡器频率，然后减去中频来实现的。[glasslinger]正在用一个 Arduino(嘿，这是一个合法的工程选择)和一个 4040 12 位二进制计数器作为预缩放器来实现这一点。Arduino 进行数学运算，然后驱动几个 74141 谢妮驱动程序，这些驱动程序将接收器的频率显示在漂亮的玻璃管中。给千位数字加上一个霓虹灯，你就有了一个四位数的显示屏，它会告诉你一个老式调幅收音机调到了什么频率。

建筑的其余部分包括修复一台旧收音机，并用现代胶水将贴面粘合，这将再持续 70 年。完成后的橱柜被打磨，显示器的边框被添加，由于[glasslinger]有了设备，他制作了一个新的长霓虹灯管，以随着收音机的音量发光。你觉得猫眼探测器很酷。

这个建筑是一个杰作，非常现代，但同时又建立在古老的技术之上。如果你有一个半小时的时间，我们强烈建议你看看下面的视频。

 [https://www.youtube.com/embed/mvCwzLowmOo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/mvCwzLowmOo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

