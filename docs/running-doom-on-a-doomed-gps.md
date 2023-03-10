# 在一个注定失败的 GPS 上运行毁灭

> 原文：<https://hackaday.com/2019/09/01/running-doom-on-a-doomed-gps/>

当你在车库拍卖中看到廉价出售的旧 GPS 导航系统时，你首先想到的是什么？我们的研究表明，100%的人会怀疑它是否会遭遇厄运；至少这是我们从现有的单一数据点得出的结论。【杰森·金】[询问并回答了关于他最近收购的问题](https://ripitapart.com/2019/08/30/hacking-into-windows-ce-and-doom-on-the-magellan-roadmate-1412-gps-receiver/)——响亮地回答了“是”。

有问题的设备是运行 Windows CE 的 Magellan RoadMate 1412。玩了一会儿后，[Jason]发现只要通过 USB 将设备连接到计算机，所有的应用程序文件就会显示为 FAT 格式的卷。用一个 [TotalCommander/CE](https://www.ghisler.com/ce2.htm) 的副本替换明显命名的“MapNavigator.exe ”,允许浏览文件系统。

这表明 CE 安装缺少了很多东西，包括 Explorer shell 和命令提示符。这两种方法都可以使用所需的命令行参数来启动 *Doom* 。幸运的是，[Jason]准备了另一个技巧，即使用 MortScript(一个脚本引擎)来启动*毁灭*可执行文件。这非常有效，经过一些调整后，他现在有了一个专用的演示盒。

我们说“演示盒”而不是“*毁灭*机器”,因为没有键盘，你实际上不能玩游戏——只能观看演示。在一次勇敢的尝试中，他连接了一个 USB OTG 连接器，但 GPS 似乎不能识别输入设备，只能识别 USB 存储设备。继续努力，[杰森]，我们很乐意看到你破解这个！

[Jason]对入侵 Windows CE 设备并不陌生。上次我们入住时，[目标是一台是德科技 DSO1102G 示波器](https://hackaday.com/2018/10/18/playing-doom-on-keysight-oscilloscope-via-windows-ce/)。

 <https://hackaday.com/wp-content/uploads/2019/09/doom-on-magellan-roadmate-gps.mp4?_=1>

[https://hackaday.com/wp-content/uploads/2019/09/doom-on-magellan-roadmate-gps.mp4](https://hackaday.com/wp-content/uploads/2019/09/doom-on-magellan-roadmate-gps.mp4)