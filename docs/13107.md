# 红外遥控转换为射频

> 原文：<https://hackaday.com/2022/03/21/ir-remote-transforms-to-rf/>

大多数消费者遥控器使用红外线来操作。这在假设设备能够看到遥控器的情况下工作得很好。但是如果你有，比方说一个在橱柜或壁橱里的接收器，红外遥控信号不能到达传感器。有些设备有遥控接收器，你可以把它伸出来，但它仍然不是很方便。这就是为什么一些设备现在使用射频遥控器。[Xtropie]使用一对廉价的 433 MHz 射频模块[将红外系统转换为射频](https://www.instructables.com/Hacked-Convert-Any-IR-Remote-Into-RF/)。你可以在下面看到一个关于这个项目的短片。

我们可能会尝试简单地在接收器上放置一个红外 LED，以便它可以将红外输入到设备传感器中，但[Xtropie]采取了不同的方法。他找到了红外传感器，并将射频接收器直接连接到它的输出端。它似乎工作，但我们可能会删除红外传感器，以确保没有冲突。

事实上，如果您拆除传感器，您可以重复使用它，并将其连接到红外发射器。不清楚如何轻松包装射频发射器和遥控器。但我们突然想到，你可以将发射器直接连接到 LED 输出端，完全避开红外传感器。如果在远程情况下没有空间，也许 3D 打印扩展可以做到这一点。

当然，没有什么能阻止你在自己的项目中使用 RF 遥控器。当然，射频遥控的另一种方式是[利用 WiFi](https://hackaday.com/2022/01/19/adding-wifi-remote-control-to-home-electronics-be-prepared-to-troubleshoot/) 。

 [https://www.youtube.com/embed/ISI_soanilc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ISI_soanilc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

