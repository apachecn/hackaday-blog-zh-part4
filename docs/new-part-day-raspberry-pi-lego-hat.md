# 新零件日:树莓皮乐高帽

> 原文：<https://hackaday.com/2021/10/21/new-part-day-raspberry-pi-lego-hat/>

Raspberry Pi 基金会在过去几年里一直在忙着生产他们自己的硅，新的电路板，现在与乐高教育团队合作，推出了一款新的帽子，以连接到乐高钉教育平台。这款新的 HAT 板可与每一款带有 40 引脚 GPIO 接头的 Raspberry Pi 板配合使用。

![](img/dc49b14889d4987c1588487e8db3936b.png)

基于 RPI2040 微控制器，它有趣地避开了哑从板，尽管它看起来像是固件关闭了(目前)，所以你必须利用预烘焙的功能，并使用提供的 python 库与它对话。

根据[文档](https://www.raspberrypi.com/documentation/accessories/build-hat.html)，Pi 和位于 HAT PCB 下方的 RPI2040 之间的通信是[明文串行](https://datasheets.raspberrypi.com/build-hat/build-hat-serial-protocol.pdf)，释放了大部分 GPIO 引脚用于其他用途。该板使用表面贴装直通型接头，允许 Pi 引脚穿过 PCB，从而可以在顶部堆叠更多的帽。奇怪的是，他们决定将 PCB 的有源部分朝下安装，以提供一个平坦的后表面来放置东西。我们怀疑该决定是为了改进 LPF2 连接器的使用，尤其是当它们是表贴器件时。

![](img/a831a1c16860ff13674c53b6958d4922.png)与乐高硬件的兼容性也有完整的记录，包括 [Spike Education portfolio](https://education.lego.com/en-gb/products/lego-education-spike-prime-expansion-set/45681) ，其中包括电机、颜色传感器、力传感器和距离传感器等。mindstorms 机器人 inventor kit as 中的某些部件也受支持。乐高还推出了一个新的部分，他们称之为“制造者板块”，这是专门为安装“SBC”而设计的，但没有指定是哪一个。显然，这看起来需要 Pi3/4 委员会，但我们会让他们来澄清其他支持。

还引入了一种新的更高功率的电源砖，它将 8V 输入到你可能已经注意到的桶形插孔中，正如你可能意识到的那样，LEGO motors 可以提供相当大的功率，试图从 Raspberry Pi GPIO 头为这些电源供电只会以失败告终。

这些年来，我们已经看到了大量的乐高黑客，这个新产品并不是我们看到的第一个黑客解决方案。先看看这个[开源](https://hackaday.com/2020/11/05/open-source-lego-controller/)*evlūno One*。然而，这款新产品是一个很好的例子，说明一家相当开放的公司与一家老牌公司合作，生产一些很酷的东西，这是一件好事。

 <https://hackaday.com/wp-content/uploads/2021/10/Raspberry-Pi-Build-HAT-Plotter.mp4?_=1>

[https://hackaday.com/wp-content/uploads/2021/10/Raspberry-Pi-Build-HAT-Plotter.mp4](https://hackaday.com/wp-content/uploads/2021/10/Raspberry-Pi-Build-HAT-Plotter.mp4)

感谢[Qes]的提示！