# 逆向工程顶场 VFD 前面板

> 原文：<https://hackaday.com/2021/08/14/reverse-engineering-a-topfield-vfd-front-panel/>

黑客喜欢真空荧光显示器(VFD)的温暖辉光，并且不缺少废弃的消费电子产品，可以从这些电子产品中取出来，以保持我们的集体零件箱库存良好。不幸的是，弄清楚如何实际驱动这些抢救出来的模块可能会很棘手。但是多亏了[Lauri Pirttiaho]的努力，我们现在有了大量关于配备了 VFD 的前面板的信息，这种面板用于 Topfield 个人录像机的几个型号。

该电路板由 Hynix HMS99C52S 微控制器供电，包括五个按钮、一个小的四字符 14 段显示屏、一个大的八字符字段和一系列媒体播放相关图标。船上还有一个实时时钟模块，以及一个红外接收器。[Lauri]告诉我们，至少有六个 Topfield 模型使用了相同的电路板，这应该可以相对容易地找到一个。

[![](img/e52c86fc4c76b9c77ded2f86903ab35f.png)](https://hackaday.com/wp-content/uploads/2021/08/topfieldvfd_detail.jpg) 在确定了连接模块和记录器的 6 针连接器的位置后，用逻辑分析仪轻轻一拨，发现它们通过 UART 通信。通过解码命令，[Lauri]能够编写一个简单的 Python 工具，让您只需一个 USB 转串行适配器就能驱动前面板。不过请记住，您需要在连接器的适当引脚上提供 17 VDC 来启动 VFD。

那是什么？你不需要整个前面板，只是想把 VFD 本身从板上拉下来？没问题。我们的人[Lauri]好心地记录了数据是如何从 Hynix 微控制器传递到显示器本身的；如果你想把屏幕从 PVR 的装饰中解放出来，关键信息。

如果你设法得到其中一个模块，[它将是定制媒体流](https://hackaday.com/2019/09/15/scratch-built-media-player-channels-1980s-design/)的理想补充。虽然我们简单地假设[把它变成一个网络控制的时钟](https://hackaday.com/2020/02/06/a-network-attached-vfd-tube-clock/)会是一个合适的选择，如果你正在寻找更简单的东西。

 [https://www.youtube.com/embed/b1bDptDE3qU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/b1bDptDE3qU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

