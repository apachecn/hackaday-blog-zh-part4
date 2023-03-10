# DEF CON 26 的所有徽章(第 2 卷)

> 原文：<https://hackaday.com/2018/08/21/all-the-badges-of-def-con-26-vol-2/>

今年的 DEF CON 上有如此多令人惊叹的非官方徽章，我不可能在一个镜头中涵盖所有这些徽章。我试图看到每一个徽章，并与每一个徽章制造商交谈——就像一次硬件旅行。在跳跃之后加入我，获得我在 DEF CON 26 上看到的大约 14 个徽章！

如果你错过了第一批，[也去看看那些徽章吧](https://hackaday.com/2018/08/14/all-the-badges-of-def-con-26-vol-1/)——甚至还有[一部 Badgelife 纪录片](https://www.youtube.com/watch?v=G2fHKRONc6U&t=10s)，你需要把它添加到你的观察列表中。好吧，我们开始吧。

## DC 皮草徽章

 [![12-dcfurs-front](img/d2fc0eb78a8a949b9b5566d6362c70f1.png "12-dcfurs-front")](https://hackaday.com/?attachment_id=320491)  [![12-dcfurs-rear](img/8098a65b365a7a2eca4b62aec72dff50.png "12-dcfurs-rear")](https://hackaday.com/?attachment_id=320492)  [![Secret codes!](img/9d0c699c21919dd097e4497a01e22f01.png "12-dcfurs-cipher")](https://hackaday.com/?attachment_id=320490) Secret codes!

有这么多有创意的硬件徽章，很难将它缩小到一个最喜欢的，但[DC furs 徽章](https://twitter.com/dcfurs)非常接近今年的最佳。我喜欢它的一个原因是艺术赋予了它标志性的外观。据我所知，这是原创的，而不是借用流行文化。镀金铜、哑光黑色阻焊膜和白色丝网的组合被用在很多徽章上，但这种设计真的很流行。最后，显示屏简单而有趣的设计产生了一些非常有趣的图案，而且它仍然足够密集，可以很好地滚动文本。

该小组在 STM32F411 的基础上制作了 600 个这样的徽章，因为它运行 MicroPython。这用于屏幕上显示的可视化，而谜题和硬件抽象层是用 c 编写的。

## 护身符钟

 [![13-vfd-clock-necklass](img/720161c93575b1ab832b04c0d598af8a.png "13-vfd-clock-necklass")](https://hackaday.com/?attachment_id=320493)  [![13-vfd-clock-stackup](img/29353b0ad72e0f62d672edfd7ec32033.png "13-vfd-clock-stackup")](https://hackaday.com/?attachment_id=320494) 

护身符时钟不完全是一个徽章，但它足够酷(足够接近)在这里提到。它使用 VFD 显示时间，在-30V 下运行。电源设计和让它离你的脖子这么近，都有点令人着迷，但太复杂了，无法在此详述。这座钟的创造者希望能把这个设计写进 for POC | |的一篇文章中，所以希望我们能在不久的将来读到它。

## 机器人先生徽章

[![](img/24602ebe44a388f90514ffaa4cdd861c.png)](https://hackaday.com/wp-content/uploads/2018/08/48-mr-robot.jpg)

MrRobotBadge 再次成为 DEF CON 26 上的热门商品。徽章艺术的一面是基于同名电视节目中反一切的吉祥物。

今年的徽章大大增加了展示的尺寸。驱动徽章的 ESP8266 不可能跟得上显示，但使用 IS31FL3741 显示驱动程序使之成为可能。它接受 I2C 命令，并依次处理 39×9 矩阵的扫描。在这种情况下，徽章上的 LED 矩阵为 18×18，左侧有一个 d-pad，右侧有两个按钮(经典的 NES 风格)。

您可以使用串行转 USB 电缆对徽章重新编程。我在徽章上看到的一个更酷的例子是康威的生活游戏。

## 蜻蜓 2 徽章

 [![19-dragonfly](img/8e69c01b1e90e5ea243c8093633777d0.png "19-dragonfly")](https://hackaday.com/?attachment_id=320603)  [![dragonfly-badge-2-wb](img/747e78d95c268b905aca0b151971fb8c.png "dragonfly-badge-2-wb")](https://hackaday.com/2018/08/21/all-the-badges-of-def-con-26-vol-2/dragonfly-badge-2-wb/) 

今年，蜻蜓徽章重返 DEF CON。你可以从[克里关于](https://hackaday.com/2018/03/05/badgelife-from-1-to-100/)话题的谈话中听到去年徽章的故事。吸取了手工组装的教训后，今年他将徽章制成面板，并进行专业组装。

为了与原版保持一致，蜻蜓徽章使用红外线相互交流，当它们分组时进行同步。(这个概念来自尼尔·斯蒂芬森的书*钻石时代*。)尽管今年它们有了更多的 led，但在同步信息方面，这两个版本仍然兼容。

克里包括附加标题，他佩戴的徽章是一个墨西哥玉米卷，一个鱿鱼脸，一顶圣诞老人帽和一份小薯条。也许这个设计应该获得最佳多插件发布奖！

## 德卢斯徽章

 [![21-deauth-bejeweled](img/b933835adafa6c93267f178f8afa5695.png "21-deauth-bejeweled")](https://hackaday.com/?attachment_id=320608)  [![deauth-badge](img/7eea2e75a8dedfa52893b400f4cf0c8f.png "deauth-badge")](https://hackaday.com/2018/08/21/all-the-badges-of-def-con-26-vol-2/deauth-badge/) 

我认为这是我今年调查的唯一一个非电子徽章。很抱歉没有对焦，宝石徽章让自动对焦变得困难。那是因为它反光性超强。[埃尔·健太郎](https://twitter.com/elkentaro)告诉我，徽章本身是 3D 打印的，经过平滑处理，然后涂上多层金色喷漆。嵌入的不仅仅是大宝石，而是数百个微小的玻璃片，填补了大宝石之间的空隙。

## 魁尔肯 15 号徽章

 [![07-queercon](img/612c56dbb649d568ce48843bbee1d257.png "07-queercon")](https://hackaday.com/?attachment_id=320483)  [![42-queercon-secret-text](img/98e1992845b90de2cc74f39ea272e601.png "42-queercon-secret-text")](https://hackaday.com/?attachment_id=320686)  [![7-queercon-microtext-lab-plate](img/89c93ed118da221facf74bcba338ac40.png "7-queercon-microtext-lab-plate")](https://hackaday.com/2018/08/21/all-the-badges-of-def-con-26-vol-2/7-queercon-microtext-lab-plate/) 

我们已经对 Queercon 徽章进行了深入的拆解，所以我不会在这里再走那条路了。这是我在 DC26 上看到的所有设计中最完美的。如果你去了硬件黑客村，你可能会看到 [MaraJade 的](https://twitter.com/CyberQueenMara)徽章修理亭，那里有你需要的一切来修理不计其数的徽章。当我停下来的时候，她给我看了一个我还没看过的有趣的花絮:来自 Portal 的蛋糕食谱是“实验室”面板设计的一部分，在铜层上用微型字体。整洁！

现在骗局已经过去了，关于 Queercon 15 徽章有各种各样的秘密。绝对值得一看。

## 闪光球(RGB)徽章

 [![38-led-ball-badge](img/e24750de66ccb45082e64e74963477ef.png "38-led-ball-badge")](https://hackaday.com/?attachment_id=320681)  [![Before all the slices are installed](img/c61fbbc5a7b73e1e6a464f6258db3834.png "blinky-ball-slices")](https://hackaday.com/2018/08/21/all-the-badges-of-def-con-26-vol-2/blinky-ball-slices/) Before all the slices are installed

光是想想这个巨型 RGB LED 球的供电要求就让我头疼。洛杉矶零空间实验室黑客的产品，我认为这是 320 LED 版本(16 片，每片 20 RGB LEDS)，但他们也有 384 LED 版本。查看他们的 Hackaday.io 项目了解更多信息——他们似乎正在众筹这些产品的生产。

## 维京船徽章

 [![22-borne-hack-rear](img/ced22001bf059ad33bbba70b17c6ba2b.png "22-borne-hack-rear")](https://hackaday.com/?attachment_id=320610)  [![22-borne-hack-front](img/42e0bbe4297d18bac4263ed9b3f6f731.png "22-borne-hack-front")](https://hackaday.com/?attachment_id=320609) 

该徽章再次很好地利用了哑光黑色/金色/白色，但增加了一种额外的红色。这个设计完美地运用了所有的元素，并加入白色的发光二极管来组成星座。这是 Thomas Flummer 的作品，他设计了去年和今年的 BornHack 徽章(本周晚些时候结束)。这个徽章看起来很壮观，所以这不是他的第一次表演也就不足为奇了。

我最感兴趣的是托马斯从其他 badgemakers 那里获得的灵感。在他的文章中，他提到了他从凯瑞·沙夫格拉斯的蜻蜓徽章中获得的灵感，这些徽章“没有关注头骨”——而是关注一些美丽的东西，而不是黑色 t 恤和与之相配的服饰。他还采纳了[乔·格兰德的光学间谍想法](https://hackaday.com/2018/06/10/joe-grand-is-hiding-data-in-plain-sight-leds-that-look-solid-but-send-a-message/)并付诸实施……那些发光二极管里隐藏着数据！

## 0x0G 徽章

 [![27-0x0G-front](img/3d92c152e7f1084c44bfd1dfcb462448.png "27-0x0G-front")](https://hackaday.com/2018/08/21/all-the-badges-of-def-con-26-vol-2/27-0x0g-front-2/)  [![27-0x0G-rear](img/fe54958a4a724b7f672bb6354bc97560.png "27-0x0G-rear")](https://hackaday.com/2018/08/21/all-the-badges-of-def-con-26-vol-2/27-0x0g-rear-2/) 

显然，谷歌每年都在 Blackhat/DEF CON 上举办一场活动，在我遇到[twitchyluid 64](https://twitter.com/twitchyliquid64)之前，我从未听说过这场活动。该徽章被设计成像一个赌场芯片，周围排列着发光二极管。制造了 520 个，每个都有红外接收器和 LED，让徽章改变彼此的图案。我认为 TwitchyLiquid 使用遥控器很棒，就像你看到的 LED 灯条一样，可以轻松控制徽章。查看更多关于[徽章库](https://github.com/google/0x0g-2018-badge)的细节。

## 疯狂的名牌徽章

 [![45-name-badge-front](img/f2ac893fc14837bfcfafac22d6772284.png "45-name-badge-front")](https://hackaday.com/?attachment_id=320691)  [![45-name-badge-rear](img/fa909f88bb23a3d1b5bb0b9fbe29b030.png "45-name-badge-rear")](https://hackaday.com/?attachment_id=320696) 

没有时间为你的定制徽章旋转板？#Badgelife 找到了方法。我喜欢看这个来自[演唱会](https://twitter.com/gigstaggart)的定制名签徽章。他说他在骗局开始前一周就决定做点什么，这就是结果。它是一大块原型板，四块电池，两个用于平滑负载的超级电容，以及 67 个并联的 led。哦对了，没有电阻。它毕竟只需要持续一个周末！

## 黑客仓库徽章

[![](img/ad05e0ceb122d0fc2c315ff890fa9024.png)](https://hackaday.com/wp-content/uploads/2018/08/49-hacker-warehouse.jpg)

[黑客仓库徽章](https://twitter.com/hackerwarehouse)是一个非常干净的设计。我觉得有趣的是，一些电路板看起来明显像 PCB，而其他的，像这个，最终看起来更像成品。文本和图形显示得如此之好，你几乎会认为电子设备隐藏在这个面板后面。

这个[徽章包装了 USB 和 WiFi 渗透测试方面的所有东西和厨房水槽](https://github.com/hackerwarehouse/HW-DC26-Badge)。试图看到所有徽章的困难之一是，你陷入了与人们一起参观的陷阱，而忘记了谈论徽章。这一个也是如此，但是我们很幸运，布莱恩·本考夫已经做了[一个深入的评论，分享了所有的细节](https://hackaday.com/2018/07/06/a-sneak-preview-of-the-hacker-warehouse-badge/)。

## DC 暗网徽章

 [![23-dc-darknet-kit](img/4d89ca9641f30d10e54a3738bd87da40.png "23-dc-darknet-kit")](https://hackaday.com/?attachment_id=321423)  [![23-dc-darknet-soldering](img/24bf11b3b49ae2eb350a68b1514fba0e.png "23-dc-darknet-soldering")](https://hackaday.com/?attachment_id=321424) 

每年我都渴望得到 DEF CON [Darknet 徽章](https://github.com/thedarknet/dc26-badge)。它的存在是为了参加一系列密码谜题，这些谜题既欢迎初学者(我，我不喜欢密码谜题，但想变得更好)也欢迎老手。这是我记忆中第一年有大量的徽章。

今年的徽章名为 Cdmc0de(命令代码)，共制作了 1200 多枚。它们以工具包的形式出现，一个志愿者团队花了大约 3 个晚上才把所有东西装进袋子里。PCB 本身已经安装了所有的表贴元件，包括 STM32 和 ESP32，它们都包含在设计中。这是暗网徽章第一次使用定制编程夹具，据说这使得闪烁过程成为一个梦想。

组装后有两个屏幕，一个窄而长的有机发光二极管和一个更大的 LCD 屏幕。徽章能够基于从基于 D-pad 和双按钮(又是经典的 NES)用户界面的用户菜单中的选择来彼此交互。内心充满困惑，但我还没有接受它们。

## 固特异飞艇

[![](img/f4bd278ae17829496faabfd87e635741.png)](https://hackaday.com/wp-content/uploads/2018/08/47-goodfear.jpg)

这是一个很棒的徽章，但没有完全通过终点线。正如你所看到的，它的设计看起来像固特异飞艇，装饰着数百个发光二极管。大约 7 英寸宽，它会给你的挂绳式珠宝增加一个令人生畏的亮点。不幸的是，在项目进入固件阶段之前，时间已经用完了，但是硬件已经准备好了。

这并没有阻止克里斯·甘梅尔享受硬件带来的乐趣。随着时间的流逝，他还推出了一个附加产品。基于 DC25 超受欢迎的“这不是相机”贴纸，他制作了一个外形像监控摄像头的附加组件，并用 DC26 分发电路板。

## DC503 徽章

[![](img/d8932d417503a6c2c3ead98a530ca64f.png)](https://hackaday.com/wp-content/uploads/2018/08/52-dc503.jpg)

DC503 徽章是我每年都要寻找的。表面上它是为波特兰地区的黑客建造的，但我认为有如此庞大的 DC503 团体的追随者，如果你想成为这个每月一次聚集在波特兰，每年在 DC 聚会的令人敬畏的人群中的一员，他们不会真的在乎你来自哪里。

今年徽章的主要特征是一个 3D 打印的扩散器，可以绕在你的手腕上。里面是一个 RGB LED 条，通过白色塑料看起来很棒的旋转图案。单驱动板夹在你和扩散器之间。在 bump in 503 派对上他们无处不在。除此之外，我没有这方面的更多信息。任何知情人士，请在下面的评论中留下详细信息。

## 黎明前再一次

今年的 DEF CON 徽章选集还没有结束。我想我可以在一个更大的装置里看完我在展会上看到的其余徽章。密切关注黑客日！