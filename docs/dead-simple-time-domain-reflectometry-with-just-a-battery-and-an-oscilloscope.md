# 只有一个电池和一个示波器的简单时域反射仪

> 原文：<https://hackaday.com/2020/12/14/dead-simple-time-domain-reflectometry-with-just-a-battery-and-an-oscilloscope/>

“时域反射仪”听起来确实需要大量昂贵的设备来完成。实际上，TDR 只是测量将脉冲注入电缆与接收到回波之间的时间，回波可能来自电缆的另一端，也可能来自沿途的故障或缺陷。这是一项有用的技术，正如[Allen Wolke(w2 aw)]向我们展示的那样，只需一节电池、一个电阻和一个示波器就可以完成。当然，还会一点数学。

当然，也有专用的时域反射计，但所有这些都只是对他的简单设置所展示的基本原理的阐述。示波器在一个通道上设置有三通连接器；三通的一侧连接到被测电缆，而另一侧的屏蔽导体连接到 9V 电池的负极。连接到中心导体的电阻器用于完成电路，它沿着测试电缆发送一个短暂的脉冲。示波器被设置成捕捉输出脉冲和返回脉冲，允许测量两者之间的时间。一些简单的数学计算给出了电缆的长度，到断层的距离，或者稍作调整，电缆的速度系数。

下面的视频显示了同轴电缆和 5e 类以太网电缆的简单工作方法。它甚至在一卷拉链电缆上工作，这有点令人惊讶。如果这种技术太简单，你总是可以详细说明一下，然后[推出你自己的 TDR 测试器](https://hackaday.com/2015/07/27/hackers-measure-cable-lengths-with-time-domain-reflectometers/)。Googly eyes 当然可选，但是推荐。

 [https://www.youtube.com/embed/z6UJPqQYzNc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/z6UJPqQYzNc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

