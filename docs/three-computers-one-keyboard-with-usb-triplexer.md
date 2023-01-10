# 三台电脑，一个带 USB 三工器的键盘

> 原文：<https://hackaday.com/2022/11/04/three-computers-one-keyboard-with-usb-triplexer/>

我们中的许多人都会遇到同一张桌子上有几台计算机的问题，为了避免混乱，我们将使用 KVM 交换机来共享外围设备。[缠头巾的工程师]对这个问题有一个有趣的解决方案，形式是 USB 三工器。这是一种根据哪个连接通电来路由 USB 数据线的设备。

电路非常简单:一个 CMOS 模拟多路复用器完成路由，一组光耦合器根据功率输入进行选择。一套 USB A 插座连接电脑，一套 USB B 插座连接外设。

我们不完全确定模拟多路复用器芯片是否适合更高速的 USB 数据速率，但由于键盘和鼠标以最慢的数据速率说话，我们认为他会成功的。不管是哪种方式，用如此普通的元件制作一个 USB 开关都有一定的难度。我们不太清楚他用显示器做了什么，但至少他的键盘和鼠标问题得到了解决。

我们介绍的其他类似开关已经[更加基本](https://hackaday.com/2016/11/12/diy-kvm-switch-lets-you-use-one-keyboard-and-mouse-with-multiple-computers/)。