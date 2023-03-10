# 把很多东西装进一个小 PCB:平方英寸项目的赢家

> 原文：<https://hackaday.com/2018/10/18/packing-a-lot-into-a-little-pcb-winners-of-the-square-inch-project/>

当你想到如今手掌中的计算能力时，你会感到难以置信。就在不久前，地板抬高的空调房里，电脑的功能远不如现在，充斥着整个区域。小型化肯定是当今的潮流。事情也一天比一天小。我们对第一个“平方英寸项目”的微小参赛作品印象深刻——该竞赛要求设计师使用 1 英寸 ² 或更少的 PCB 因此我们决定通过[平方英寸项目](https://hackaday.io/contest/160135-the-return-of-the-square-inch-project)的回归来带回它。规则真的很简单:用一平方英寸的 PCB 做一个东西。

## 大奖

很难选出，但大奖得主只能有一个。这一次，这项荣誉颁给了[Danny FR],他设计了一个非常小的机器人智能马达驱动器。小电路板通过 I2C 链接到微控制器，并通过 RPM 反馈进行 PID 控制。不需要 H 桥或任何复杂的控制电子设备，这些都在船上。

[![](img/b64751b2f51207d0e752e4e0c25a87e8.png)](https://hackaday.com/wp-content/uploads/2018/10/motor.png)

该板非常适合马达，可以轻松构建移动项目。这是大奖，但也有其他一些伟大的作品赢得了特定类别的奖项。

## 最佳项目

[Drix]喜欢知道东西在哪里。蜂巢追踪器使用激光“灯塔”扫过房间。带有专用硬件模块的特殊微控制器读取激光，并以极高的精度对其相对于灯塔的位置进行三角测量。一张照片胜过千言万语，所以:

 [![laser](img/a142e3e3d1377fcb9f43e89921026bc1.png "laser")](https://hackaday.com/2018/10/18/packing-a-lot-into-a-little-pcb-winners-of-the-square-inch-project/laser-27/)  [![hive](img/9343aa5cfd04bcd5e436d7419b07fe1c.png "hive")](https://hackaday.com/2018/10/18/packing-a-lot-into-a-little-pcb-winners-of-the-square-inch-project/hive/) 

激光的高速读取使用“[可编程外围互连](https://hackaday.io/project/160182-hivetracker/log/150468-miniaturization-idea-validation)”——这是北欧 ble 微控制器的一项功能，让芯片在不中断处理器的情况下读取硬件中的时间戳。这些小电路板连接到一个也很小的集线器板上。

我们是黑客，所以我们认为一些裸露的 PCB 连接到另一个 PCB 可以是艺术。但是大多数人的想法是不同的。

## 最佳艺术项目

![](img/468957bea379ba4f0d18b33d8bc6ae15.png)

如果你经常在 Hackaday.io 上闲逛，你会认出[ꝺeshipu]，他的词条是你马上就知道可以使用的东西之一，但当你使用它时，也会让你脸上露出一丝微笑。您多久需要将一些 led 插入试验板一次？为什么不用[彩虹水母](https://hackaday.io/project/159022-rainbow-jellyfish)来做呢？

电路操作应该很明显。我们真的很喜欢彩色编码的线路。你可能至少需要两个这样的人，这样他们就可以互相陪伴了。你甚至可以把它作为徽章的一部分。

## 最佳社交媒体奖

 [https://www.youtube.com/embed/zghHKhZsF10?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/zghHKhZsF10?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



说到徽章，[nwmaker]制作了一个看起来像另一种动物的徽章——一种叫做 PurpleSnowy 的猫头鹰。同样，线路很简单，但是这个项目吸引我们眼球的是它在社交媒体上的推广。也许可爱的猫头鹰更容易传播，但我们喜欢它。

## 最佳文档

[![](img/73a29ec2d2bbdf7bde808fc8c2be6db1.png)](https://hackaday.com/wp-content/uploads/2018/10/spec1.png) 【克里斯·韦纳】(记得那个名字)，建造了一个非常高科技的[光谱仪](https://hackaday.io/project/143014-compact-25-spectrometer)项目。它不仅体积小，而且 25 美元的价格也很便宜。该项目使用 AMS AS7265X 3 芯片组来提供 18 通道、20 纳米 FWHM 光谱仪。文档做得非常好，我们对电路板上芯片的安装印象深刻。

## 许多亚军

我们有太多优秀的参赛作品，很难挑选，所以我们提名了几个亚军。

孙波帧抓取器使用 FPGA 从前视红外玻色子相机中捕捉图像。

[克里斯·维纳的]高科技 25 美元分光计项目(上图)也获得了亚军，[克里斯]还因能[闻和听](https://hackaday.io/project/19649-stm32l4-sensor-tile)的传感器而被认可。

如果你想要一些与科学无关的东西，由[zakqwy]开发的 [Rotovis-Mod1](https://hackaday.io/project/27829-rotovis-mod1) 可以更容易地建立视觉显示器的持久性。当然，作为黑客，我们喜欢示波器和(马克·奥莫的)[一英寸大小的 20 msps 示波器](https://hackaday.io/project/160802-1-square-inch-20msps-oscilloscope)激发了我们制作一些非常酷的仪表板的想象力。

你真的应该看看所有参赛作品——它们太棒了。[Kris]真的全力以赴，获得了两个亚军位置和最佳文档奖。

## 概述:

说到奖品，大奖是 500 美元，其他奖品获得 100 美元的 Tindie 礼券。多亏了奥什公园，亚军还得到了价值 100 美元的奥什公园礼品卡——这可是一大堆一英寸厚的多氯联苯。

*   [大奖:机器人智能电机驱动器](https://hackaday.io/project/158429)
*   最佳项目:蜂巢追踪器
*   最佳艺术元素:彩虹水母
*   [最佳社交媒体:紫雪](https://hackaday.io/project/160328)
*   最佳文档:小巧、25 美元的光谱仪
*   [亚军:紧凑型，25 美元光谱仪](https://hackaday.io/project/143014)
*   [亚军:玻色子帧抓取器](https://hackaday.io/project/160928)
*   [亚军:Rotovis-Mod1](https://hackaday.io/project/27829)
*   [亚军:STM32L4 感应贴片](https://hackaday.io/project/19649)
*   [亚军:1 平方英寸 20msps 示波器](https://hackaday.io/project/160802)

这会是我们最后一次平方英寸的比赛吗？magic 8 ball 说可能不会，所以不要停止思考小问题，寻找机会在下一次比赛中进入你的设计。