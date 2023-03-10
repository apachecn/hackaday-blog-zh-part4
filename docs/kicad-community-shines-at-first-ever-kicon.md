# KiCad 社区首次亮相 KiCon

> 原文：<https://hackaday.com/2019/04/30/kicad-community-shines-at-first-ever-kicon/>

上周末是 [KiCon](https://kicad-kicon.com) ，来自世界各地使用 KiCad 开源 EDA 软件的硬件开发者的聚会。这包括许多推动开发的软件工程师，在业务中使用 KiCad 的人，以及那些仅仅因为 KiCad 是任何人都可以使用的专业质量工具而喜欢它的人。

从硬件展示和讲解，到一系列的演讲，以及每晚的社交活动，两天(加)的时间里安排了如此之多的活动。休息之后，请和我一起对 2019 KiCon 上的人和硬件进行一次旋风之旅。

## 社区

[![](img/a8294c3189e15f0f20570519fdf41fb5.png)](https://hackaday.com/wp-content/uploads/2019/04/KiCon-hackaday-meetup-festivities.jpg)

Above: Side area at Hackaday afterparty
Top of Article: Main room at Hackaday afterparty

Chris Gammell 组织了这次会议，他做得非常出色。该活动超越了 mHub 的围墙，KiCon 就是在这个面向制造业的合作空间举行的，活动期间还包括三个晚上的社交活动。

周四晚上来到镇上的每个人都来到了芝加哥硬件欢乐时光，度过了一个漫长的夜晚，包括许多硬件演示。周五晚上谈判结束时，我们跳上火车，在[泵站开派对:一个](https://pumpingstationone.org/)，城市北边的一个巨大的黑客空间。在 KiCon 正式结束后，Hackaday 帮助举办了一个后续派对，这种乐趣仍在继续。所有这三个晚上都被打包，并提供了非常需要的计划外时间，以满足每个人的需求，并赶上他们在硬件领域的进展。

## 徽章

 [![Front of badge (two additional resistors is a hack to keep the USB power bank from sleeping)](img/14a49dc3982d02d3fc99c8ac8705a3b3.png "KiCon2019-badge-front")](https://hackaday.com/2019/04/30/kicad-community-shines-at-first-ever-kicon/kicon2019-badge-front/) Front of badge (two additional resistors is a hack to keep the USB power bank from sleeping) [![Back of badge](img/ab5a3e62577ff3b385afbaeab0a192e7.png "KiCon2019-badge-back")](https://hackaday.com/2019/04/30/kicad-community-shines-at-first-ever-kicon/kicon2019-badge-back/) Back of badge

令我高兴的是，有一个由 Maciej Sumiński 设计的 KiCon 硬件徽章。这款简单的电路板功能强大，可用作 8 通道逻辑分析仪、简单的示波器、USB 转 UART 以及通过 USB 控制 GPIO 的能力。[硬件设计](https://github.com/orsonmmz/kicon19-badge-hw)基于 LQFP-64 Atmel/Microchip atsam 4 SD 16 ba，它包括一个庞大的~~1mb~~160 kB RAM，运行频率为 120 MHz。用户界面是带有四个用户按钮的有机发光二极管显示器。

> 我添加了一点动画作为我的 [#KiCon2019](https://twitter.com/hashtag/KiCon2019?src=hash&ref_src=twsrc%5Etfw) 徽章黑客。(轴向电阻是防止移动电源休眠的黑客)【pic.twitter.com/HcvxE8j40Y 
> 
> — Mike Szczys (@szczys) [April 27, 2019](https://twitter.com/szczys/status/1122268646108225536?ref_src=twsrc%5Etfw)

一个小型便携式电池是电源。徽章电量太低，无法保持电池唤醒，但可以通过在去耦电容上焊接一些电阻来解决这个问题，这样我就可以在会议期间显示自己的动画作为我的姓名徽章。

## 会谈

关于 EDA 软件你能说多少？像任何好的工具一样，用途是无穷无尽的，我喜欢听独特的用例，就像我喜欢听如何克服它们一样。会谈被记录了下来，我将会关注那些可能被公开的内容，因为两个会谈地点让我不可能看到所有的内容。(更新:它们将在[上下文电子频道](https://www.youtube.com/channel/UCkJRycUz2CylxpiP-zMePow)上发布)

我当然不会错过的一个演讲是韦恩·斯坦博作为 KiCad 项目负责人的主题演讲。这一直是，并且仍然是所有相关人员的爱的工作。但是好消息是 Wayne 已经被雇佣全职从事 KiCad 项目，这是 T2 Wit T3 公司对开源社区的一个不可思议的贡献。这个消息是在讨论了版本 6 的计划后，在演讲结束时发布的；新的逻辑示意图和符号库文件格式、逻辑示意图的 Python 脚本、从符号库到逻辑示意图编辑器的拖放、阴影区域填充、SVG 到电路板的导入、ratsnest 弯曲、着色和可见性支持都是提到的工作。

![](img/3c4159d9e4140181dbeb9c8dbf8228c0.png)

Top: Developers Panel
Bottom: Manufacturers Panel

座谈会是我在会谈中最喜欢的部分。这些会议有多人在台上，由主持人引导对话，观众可以自由提问。来自一个非常感兴趣的人群，问题是深思熟虑的，这些问题引导了 KiCad 开发者小组和制造商小组令人难以置信的讨论。

## 黑客们

KiCon 出了很多硬件设计师，他们没有把自己的宠物项目留在家里。

 [![Assembled ski goggle blinkies](img/2ed4d8eb09155ddbab8a1a483a19d619.png "KiCon2019-goggles-assembled")](https://hackaday.com/2019/04/30/kicad-community-shines-at-first-ever-kicon/kicon2019-goggles-assembled/) Assembled ski goggle blinkies [![Front of board](img/dc5a262332e79c2ccc4d125b66d99b33.png "KiCon2019-goggles-board-front")](https://hackaday.com/2019/04/30/kicad-community-shines-at-first-ever-kicon/kicon2019-goggles-board-front/) Front of board [![back of board](img/3e3835bb0aaef8fa081c4c0668726eec.png "KiCon2019-goggles-board-back")](https://hackaday.com/2019/04/30/kicad-community-shines-at-first-ever-kicon/kicon2019-goggles-board-back/) back of board [![Curved control board and auto-generated jig](img/0a4281bdcf524f4fe9a008ded00178a5.png "KiCon2019-goggles-programming-jig")](https://hackaday.com/2019/04/30/kicad-community-shines-at-first-ever-kicon/kicon2019-goggles-programming-jig/) Curved control board and auto-generated jig

这种滑雪护目镜 LED 板本身就很迷人，但设计过程也是乌列尔·盖伊在大会上的演讲主题。他为 KiCad 编写了一个 C#包装器，它将重复放置 LED 和电路板切口，让你透过矩阵看到。但是真正令人眼花缭乱的是弯曲控制板的夹具——夹具是自动生成的，几乎每个制造过任何东西的人都会对这个特性感兴趣。

 [![Morgan's coffin-badge is high art](img/c74f2114357c76155a0b88db9186575e.png "KiCon2019-coffin-badge")](https://hackaday.com/2019/04/30/kicad-community-shines-at-first-ever-kicon/kicon2019-coffin-badge/) Morgan’s coffin-badge is high art [![This LED matrix is programmed through the two phototransistors on the top edge](img/c444690daeae887a9014f9cd220c187b.png "KiCon2019-blinky-grid")](https://hackaday.com/2019/04/30/kicad-community-shines-at-first-ever-kicon/kicon2019-blinky-grid/) This LED matrix is programmed through the two phototransistors on the top edge

摩根出现在周四晚上的聚会上，戴着他制作的徽章，简直完美。顶盖是一个 PCB 挡板，底部有粉红色的 led，用于照亮内部的电子设备和电池。外壳的侧面和背面也是 PCB，一起开槽，侧面有控制按钮。顶部有一个 PCB 挂绳孔眼，底部有一个 USB 充电端口。

我遇到了 Wayne 和 Layne 后面的工程师，他们都穿着他们的[我可以焊接 SMT](https://www.wayneandlayne.com/projects/blinky-smt/) 板。我喜欢这些，因为它们是用顶部边缘的光电晶体管进行光学编程的。

 [![Airwire as art](img/6150b5b48aef649679ef113b8f8c36d8.png "KiCon2019-mohit-snake-rear")](https://hackaday.com/2019/04/30/kicad-community-shines-at-first-ever-kicon/kicon2019-mohit-snake-rear/) Airwire as art [![Thumbsitck snake game](img/0dfcb6f962ee1bad170978ec2b8cf2d8.png "KiCon2019-mohit-snake-front")](https://hackaday.com/2019/04/30/kicad-community-shines-at-first-ever-kicon/kicon2019-mohit-snake-front/) Thumbsitck snake game [![Fitness tracker](img/dcfd69e05adb1cb10b468dc3792a4071.png "KiCon2019-watch-board")](https://hackaday.com/2019/04/30/kicad-community-shines-at-first-ever-kicon/kicon2019-watch-board/) Fitness tracker [![Castellation and SMT resistors as watch band slot](img/80e51e6148f7e38da8455b181b0e4fb9.png "KiCon2019-watch-strap")](https://hackaday.com/2019/04/30/kicad-community-shines-at-first-ever-kicon/kicon2019-watch-strap/) Castellation and SMT resistors as watch band slot

你可能已经看过莫希特·博伊特建造的令人难以置信的赛道雕塑。他带来了一个华丽的蛇游戏，有一个木柄、拇指棒和无线 LED 矩阵。他告诉我他把它放在鹈鹕箱里运输以确保安全。

上面的手表是乔尔·墨菲正在设计的健身追踪器。它有一个步伐跟踪器(硅实际上进行检测步伐的处理)和一个心率监视器。乔尔连接表带的技术很有趣，耳孔是一个城堡，顶部和底部有一个表面贴装电阻，以保持耳到位。

 [![Pinebook prototype teardown](img/05b10d9ddde308e87f2ddecc01646c53.png "KiCon2019-pinebook-teardown")](https://hackaday.com/2019/04/30/kicad-community-shines-at-first-ever-kicon/kicon2019-pinebook-teardown/) Pinebook prototype teardown [![Eurorack face plate](img/3f3f45955d19c77200f1930a62f55a68.png "KiCon2019-eurorack-back")](https://hackaday.com/2019/04/30/kicad-community-shines-at-first-ever-kicon/kicon2019-eurorack-back/) Eurorack face plate [![Faceplate is metal-substrate PCB](img/816370431ec98372068e37038addc0f3.png "KiCon2019-eurorack-front")](https://hackaday.com/2019/04/30/kicad-community-shines-at-first-ever-kicon/kicon2019-eurorack-front/) Faceplate is metal-substrate PCB

Eric Carr 带着一箱(原型？)松本笔记本电脑。当然，人们开始拿出工具进行拆卸！我也很高兴看到这里显示的 Eurorack 面板，这是一个用铝基板制造的 PCB。显然，这是使用高功率 led 的 PCB 设计的常见选择。

这次会议聚集了许多了不起的人来庆祝使用开源工具而不仅仅是 KiCad 的硬件设计。我了解了 3D 建模，我听到了一些关于制造商如何构建我们发送给他们的设计的见解，我还直接听到了驱动 KiCad 的软件工程师的意见。在两天的会议中实在是有太多的事情要做了——尽管我们仍然尽力去做每一件事。我想我可以代表所有参与其中的人说，这次比赛进行得很顺利，我已经等不及下一次 KiCon 了！