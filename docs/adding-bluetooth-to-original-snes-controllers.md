# 在原有的 SNES 控制器上增加蓝牙功能

> 原文：<https://hackaday.com/2018/10/10/adding-bluetooth-to-original-snes-controllers/>

有很多公司在卖无线超级任天堂风格的控制器。你可以在亚马逊上买到任何数量的现代平板电脑，至少有点像任天堂传奇的 1990 年代游戏机的外观。他们有各种各样的铃铛和口哨，蓝牙，USB-C，模拟棒等。但他们都不是合法的 SNES 控制者，对一些人来说这还不够好。

[![](img/e9160a73d14b03f090d6bc074be3f27a.png)](https://hackaday.com/wp-content/uploads/2018/10/btsnes_detail1.jpg)【sjm 4306】就是这样的人。他想给合法的第一方 SNES 控制器添加蓝牙和其他一些现代的细节，所以他从易贝拿了一个坏掉的控制器，开始着手移植他的定制硬件。最终结果适用于任天堂的“经典版”游戏机，但如果你更喜欢你的经典游戏仿真版，这个概念也可以适用于原始游戏机以及电脑。

一个定制的 ATMEGA328P 供电板轮询控制器的 SPI 串行移位寄存器，方式与最初的 SNES 非常相似。然后，它获取这些按钮状态，并使用 HC-05 蓝牙模块通过 UART 发送出去。控制器由 330 mAh 3.7V 电池供电，充电电路允许使用标准 USB 电缆轻松为控制器充电。

控制器上特别好的一点是为状态 led 使用了定制的光导管。[sjm4306]通过采用透明的 PLA 3D 打印机细丝，加热并展平末端，然后打磨光滑来制作它们。这为光线提供了漫射效果，我们不得不说它看起来非常好。这绝对是一个为将来存档的提示。

在接收端，这个项目的灵感来自于我们去年推出的[定制 NES 经典版 Advantage 控制器](https://hackaday.com/2017/05/19/a-diy-nes-advantage-controller-for-the-nes-classic/)，并借用了创作者【bbtinkerer】的工作，让他的接收器硬件通过 I2C 与经典控制台进行对话。

我们已经看到了许多为经典超级任天堂控制器[增加无线功能](https://hackaday.com/2015/02/20/snes-controller-modified-to-be-completely-wireless/)的[项目，但大多数都比这个](https://hackaday.com/2013/11/19/wireless-snes-controller-for-logitech-receiver/)更具侵入性。我们喜欢读取控制器原始硬件的想法，而不是完全摧毁它。

 [https://www.youtube.com/embed/AcUOiHgEM0c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/AcUOiHgEM0c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

