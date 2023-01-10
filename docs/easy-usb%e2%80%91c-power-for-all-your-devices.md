# 为您的所有设备提供便捷的 USB C 电源

> 原文：<https://hackaday.com/2021/04/21/easy-usb%e2%80%91c-power-for-all-your-devices/>

[Mansour Behabadi]希望利用尽可能简单的硬件设计来利用 USB-C 的高功率能力。经过一些研究和实验原型，他设计了[fpx——一种易于使用的 USB-C 电源传输板](https://blog.oxplot.com/fpx/)。fpx 是他之前的 USB PD 项目[的改进版，我们之前曾重点介绍过该项目。然而，USB PD 协议的实际实现可能是一片荆棘。协商电力输送通常需要一个专用 PD 控制器和一个用于用户控制的微控制器。](https://hackaday.com/2019/10/18/usb-power-delivery-for-all-the-things/)

利用 USB PD，USB-C 端口可以配置为源、宿或两者兼而有之，并允许连接的设备协商最高 100 W (20 V，5 A)的功率。fpx 基于流行的 STUSB4500 PD 控制器，该控制器执行大部分 PD 繁重任务。为了对 STUSB4500 进行编程，他使用了 ATtiny 816 微控制器，其 UPDI 编程和调试接口消耗的电路板面积更低。

然而，有一点不同的是 fpx 的编程方式——通过从任何可以显示网页的设备发送二进制黑白闪光。使用光并不是一种特别新的编程方式。我们已经看到它在近十年前被[Wayne 和 Layne](https://store.wayneandlayne.com/category/blinky.html) 用于他们的 [Blinky PoV](https://www.wayneandlayne.com/blinky_programmer/) 项目，后来被[电动 Imp 的 BlinkUp 应用](https://hackaday.com/2012/09/04/hands-on-with-the-electric-imp/)使用。fpx 使用类似的方法从屏幕上读取闪光，这些闪光由连接到 ATtiny 的光电晶体管接收。ATtiny 然后通过 I ² C 与 STUSB4500 通信。这消除了对特殊软件或编程 IDE 的需求，并且不需要任何物理电缆连接。查看[Mansour]的博客，他向我们详细介绍了他是如何成功应对光学编程挑战的。

许多商用 USB PD 假目标/检测器/触发板使用焊接跳线或带 RGB LED 的开关来调节功率输出(PDO)。[曼苏尔]的方法可能更稳健可靠一点。STUSB4500 可以存储两个独立的 PDO 值，并可以根据其能力与源进行协商。如果信号源无法提供这些选项，fpx 可以要求最低 5 V / 100 mA 设置，或者禁用输出。fpx 是一个开源项目，可以在 [Github](https://github.com/oxplot/fpx) 上访问。休息之后，请观看视频，了解 fpx 的概况。

 [https://www.youtube.com/embed/5ij_mtj6CPs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5ij_mtj6CPs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



谢谢你的提示，[莱西]