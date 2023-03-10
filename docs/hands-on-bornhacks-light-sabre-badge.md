# 动手:博恩哈克的轻型佩剑徽章

> 原文：<https://hackaday.com/2019/09/13/hands-on-bornhacks-light-sabre-badge/>

仿照轻型马刀刀柄的徽章？是的，请！这个[星球大战主题的硬件](https://github.com/bornhack/badge2019/tree/hardware)是硬件设计师 Thomas Flummer 为上个月在丹麦举行的 2019 BornHack 大会所做的作品。(如果这是你第一次听说这件事，请看我对这件事的综述。)

[![It's not a badge but a light sabre! The front of the BornHack 2019 badge.](img/9859713b338b7fc5be419d2b4e0cdd87.png)](https://hackaday.com/wp-content/uploads/2019/08/bornhack-badge-front.jpg)

It’s not a badge but a light sabre! The front of the BornHack 2019 badge.

它非常适合手，两个 AA 电池座的巧妙侧面放置(这是我们在 2016 年 Hackday Superconference 徽章上首次看到的一个技巧),它还可以让任何突出的焊点远离衣服。在徽章的中心是 240×240 像素的彩色显示屏，它也隐藏了硅实验室 Happy Gecko 处理器及其周围的组件。当你用左手握住大拇指时，屏幕左侧电路板边缘的三个按钮非常适合你的拇指——如果你在参观云之城贝斯平时碰巧把右手落下了，这是一个不错的选择。

在电池座之间有一个四向操纵杆、两个按钮和一个 6 针附加连接器。在它的上方是一个微型 SD 卡插座和一个微型 USB 插座，在它们的上方是一个红外发射器和接收器。所有硬件都在 PCB 的正面，背面没有元件(除了电池的焊点)。但在那里你会发现一组串行和 I2C 接口的裸露焊盘。

## 轻量级工具链使编码变得容易

[![The badge from behind.](img/0a092247b46369cf41c92f409e735ef7.png)](https://hackaday.com/wp-content/uploads/2019/08/bornhack-badge-back.jpg)

The badge from behind.

插入一对 AA 电池并按下电源按钮会在屏幕上显示一个 BornHack 标志，按下按钮会显示一个菜单。发货时有一个事件时间表，一个按钮测试，一个位图显示，和一个红外数据转储应用程序。

如你所料，这是一个可破解的徽章，所有者可以为其编写自己的软件。这是对之前 BornHack 徽章的发展，而[固件](https://github.com/bornhack/badge2019)开发者 Emil Renner Berthing 已经成功实现了不可能的事情，并使其变得容易实现，而无需求助于 MicroPython 之类的解释语言。一个 apt-get 就能快速安装 arm-none-eabi-gcc 工具链，构建自己的 C 应用并添加到菜单中非常简单。我是在我的帐篷里用 Chromebook 做的，经验告诉我这通常非常困难。

## 通常的初期问题

[![Some of my fellow BornHack 2019 badge production line workers.](img/966fcd39d7e17a594985da4691fae2ed.png)](https://hackaday.com/wp-content/uploads/2019/08/bornhack-badge-production-line.jpg)

Some of my fellow BornHack 2019 badge production line workers.

这样，徽章本身就是一个简单且设计良好的徽章，没有太多的复杂性，但足够简单，易于开发。关于它的发展还有一个更深层次的故事，这是几天后在德国的混沌交流营喝酒时两人告诉我的。他们都是徽章生产的老手，但他们仍然有组件供应问题和时间限制的故事。特别是有些部件不能及时运到 PCBA，导致营地开始时没有一块木板是完整的。毫不奇怪，社区出来帮助这个项目走向完成。徽章组装团队包括丹麦人，一个来自荷兰村的庞大团体，我也加入了乐趣。第一天，我们在近 500 个徽章上焊接了一些表面贴装部件、显示器、电池和 SAO 连接器，故障比一只手的手指还要少。

我问了一下徽章硬件，比如为什么除了 SAO 之外它没有扩展能力。答案很简单，Silicon Labs 处理器是一款功能强大的设备，但其引脚数量有限，导致没有可用的备件。事实上，有些 pin 码是共享的，例如 SD 卡和红外线。红外有点不寻常，它不是像电视遥控器那样使用副载波，而是简单地将 LED 和光电晶体管连接到 GPIOs。这使它的范围非常小，但实际上这并不重要，因为交易是在很近的地方进行的。

总之，BornHack 徽章是一个简单的设计，很好地完成了它的工作，并且比你想象的更容易编程。它得益于其在以往 BornHack 活动中的传承，并为徽章系列增添了一抹亮丽的美学色彩。