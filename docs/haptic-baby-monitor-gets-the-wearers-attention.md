# 触觉婴儿监视器引起佩戴者的注意

> 原文：<https://hackaday.com/2022/08/11/haptic-baby-monitor-gets-the-wearers-attention/>

任何一个睡过早上闹钟的人都会告诉你，声音，即使是刺耳的声音，也不总是能把一个人从沉睡中唤醒。同样，在半夜听到显示器另一端的婴儿哭声也不一定会吵醒父母。那么解决办法是什么呢？由 Guy Dupont 发明的这个触觉婴儿监视器看起来很有前途。

[Guy]从 VTech 拿起一个相当标准的婴儿监视器，打开它，看看他如何将振动电机连接到原始电路中。他最初认为他必须做一些信号处理魔术来计算音频的振幅，但后来他意识到，设备前面的五个发光二极管点亮来指示音频水平已经为他做了艰苦的工作。

[![](img/5d091d89cfe2867766da61f5e5af5c8b.png)](https://hackaday.com/wp-content/uploads/2022/08/hapticmonitor_detail.jpg)

Detecting audio level by reading the status of the LEDs.

因此，他将每个 led 连接到 Seeed Studio XIAO nRF52840 微控制器的引脚上，并编写了一些代码，每秒钟可以轮询它们的状态几百次。将发光二极管的总数除以当前点亮的发光二极管的数量，得到一个很好的平均值，他可以用这个平均值来设置他内置在弹性臂带中的振动马达的强度。

另外，[Guy]还利用 XIAO 的蓝牙功能提供了一个基本的配置服务——只需在你的电脑或手机上用蓝牙串行应用程序连接到 MCU，并发出 0 到 10 之间的值来增加电机的强度。还有一个 BLE 特征，可以从客户端设备读取，以确定当前检测到的音频幅度，这可以用来绘制婴儿随着时间的推移睡得有多好。或者，如视频结尾所示，你可以用它来玩 *Flappy Bird* 。

这是一个优雅的修改，可能会为那些需要额外帮助来监视他们的微型人类的父母带来希望。这不是我们第一次看到[黑客试图改进经典的婴儿监视器](https://hackaday.com/2022/07/23/machine-learning-baby-monitor-prevents-the-hunger-games/)，但这可以说是我们迄今为止看到的最平易近人的尝试。

 [https://www.youtube.com/embed/HMZgRwgJ348?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/HMZgRwgJ348?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

