# 自动标签分配器，可快速贴标签

> 原文：<https://hackaday.com/2020/10/28/an-automatic-label-dispenser-for-quicker-stickers/>

如果你有任何类型的业务，很可能在这个过程中的某个时候会涉及到贴纸。更准确地说，这需要你一张接一张地撕掉贴纸，慢慢地浪费时间，一步步走向重复性压力伤害。当你可以让一台机器为你做这件事的时候，为什么要对自己做呢？

这正是[创新先生]的自动标签分发机背后的想法。他所要做的就是把标签卷装起来，输入每个标签的长度，然后机器就开动了，向前推进，分发和收回空纸。事实上，这就是它的工作原理:收线盘位于 NEMA-17 步进电机的轴上，该电机从 Arduino Nano 和 A4988 电机驱动器获得指令。我们最喜欢的部分是位于准备拿走的贴纸下方的红外传感器——机器不会给另一张贴纸喂食，直到它感应到你拿走了前一张贴纸。休息之后，我们继续演示和制作视频。

我们最喜欢的另一件事是,[创新先生]似乎使用了与他的[古怪的快速绕线器](https://hackaday.com/2020/10/20/arduino-bobbin-winding-machine-is-freaky-fast/)相同的 PCB。

 [https://www.youtube.com/embed/IGeIINUt_no?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/IGeIINUt_no?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

