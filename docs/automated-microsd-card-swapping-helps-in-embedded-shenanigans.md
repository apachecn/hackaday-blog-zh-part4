# 自动 MicroSD 卡交换有助于嵌入式恶作剧

> 原文：<https://hackaday.com/2022/08/08/automated-microsd-card-swapping-helps-in-embedded-shenanigans/>

[Saulius Lukse]似乎一直在运行 Linux 的单板计算机上工作。很自然，这是从 microSD 卡启动的——随着开发的进行，该卡必须一直重新成像。厌倦了在 SBC 和 SD 读卡器之间不断插拔 microSD 卡，【sau lius】[开始寻找一种更加自动化的解决方案](https://www.kurokesu.com/main/2022/08/02/ethernet-camera-module-build-log-5-automated-flashing/)——不久他就发现了[的 SDWire 项目，](https://wiki.tizen.org/SDWire)这是一种硬件工具，可以让你在 DUT(被测设备)和你的个人电脑之间交换卡，而不涉及任何移动部件。

显然，SDWire 是 Tizen 项目的一个分支，旨在帮助设备开发，无论是单板计算机还是智能手机。想法很简单——将 MicroSD 卡插入 SDWire 板，将 SDWire 插入嵌入式设备的 MicroSD 插槽，然后将 USB 电缆从 SDWire 连接到开发计算机。这样，如果你需要刷新你正在摆弄的 SBC 上的固件，你只需要通过 USB 电缆向 SDWire 板发出命令，MicroSD 卡就会作为存储驱动器出现在你的电脑上。SDWire 是一个完全开源的项目，无论是硬件还是软件，你也可以在网上购买预先组装好的电路板。

这种开发时间的缩短有助于自动化测试之类的事情，但它也大大加快了您的开发速度，节省了您在迭代之间的时间，将您从所有微小的 SD 卡摆弄中解放出来，并让您在黑客攻击中获得更多的乐趣。显然需要一个像 SDWire 这样的项目，因为我们已经看到一个黑客[使用突破组装这样一个设备](https://hackaday.com/2014/06/08/the-in-circuit-sd-card-switch/)。