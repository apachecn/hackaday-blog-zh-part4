# 一个小小的重新布线教会了 3 个新把戏下的创造力

> 原文：<https://hackaday.com/2020/02/14/a-little-rewiring-teaches-a-creality-ender-3-new-tricks/>

Creality Ender 3 是新一波廉价 3D 打印机的一部分，许多在线零售商以不到 250 美元的价格出售。为了钱，很难抱怨这台机器，它更适合任何人希望让他们的第一步进入 FDM 印刷世界。但是肯定还有改进的空间，[正如【Simon】在最近的博客文章](https://simons.tech.blog/2020/01/19/creality-ender-3-v-1-1-3-tmc2208-uart-mod/)中所展示的，一点点努力就能让这款入门级打印机更上一层楼。

第一步是用更现代的东西替换打印机的步进驱动器。通常情况下，Ender 3 使用普通的 A4988 驱动程序，但是[Simon]想用更新的 Trinamic 驱动程序替换它们，这样可以提供更安静的操作。幸运的是，Trinamic 是 A4988 的替代产品，安装相对容易。你需要更换几个电容，并从电路板上移除一些电阻，以使每个人都表现良好，但这不应该对任何知道如何使用烙铁的人构成挑战。

除了运行更安静的步进器之外，Trinamic TMC2208 驱动器还提供直接 UART 控制模式。当然，Ender 的电路板从来不是为此设计的，所以 MCU 没有足够的空闲引脚来与三个驱动器(X、Y 和 Z 轴)建立串行通信。但是[Simon]意识到，如果他牺牲了板上的 SD 卡插槽，控制器上的六个空闲引脚可以被切断并重新连接到驱动器的 UART 引脚。

结合 Klipper 固件，这些相对较小的修改使他能够[以远高于](https://hackaday.com/2017/12/26/fast-3d-printing-with-raspberry-pi-but-not-how-you-think/)之前的速度试验打印。考虑到几年前一台 200 美元左右的打印机会给你带来的那种[般的头疼，这些新机器的能力令人印象深刻；即使需要一些调整。](https://hackaday.com/2017/12/08/how-cheap-can-a-3d-printer-get-the-anet-a8/)