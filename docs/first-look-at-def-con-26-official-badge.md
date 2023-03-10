# 先看 DEF CON 26 官方徽章

> 原文：<https://hackaday.com/2018/08/09/first-look-at-def-con-26-official-badge/>

令每个人高兴的是，今年的官方 DEF CON 徽章是一个充满娱乐的电子徽章。当然有 blinky，董事会是艺术，每个人都希望可能得到一个(据传 27，000+制造)如果他们没有用完。但是 DEF CON 上的徽章竞赛是传奇式的——解决所有的谜题，你将获得梦寐以求的黑色徽章。

这个徽章的创造者对 Hackaday 社区来说并不陌生。自豪地显示在电路板和固件上，我们发现[玩具制造商](https://twitter.com/tymkrs)是今年把所有东西都放在这条线上的人。来自明尼苏达州的动态硬件集体致敬。在徽章的世界里，没有比这更大的高压锅了，他们奇迹般地成功了。让我们看看里面所有的好东西。

最重要的是，[成为 Hackaday.io](https://hackaday.io/project/160333/token/082005aa-c1c9-4424-8b68-fb09ba80ca7d) [DC26 徽章解决项目](https://hackaday.io/project/160333-def-con-26-official-badge-hacking)页面的团队成员，帮助发现这个徽章所涉及的一切。好了，现在我们开始吧！

## 硬件

[![](img/c3acf91c5fbd52f85dfb3e4e2e9cf3b8.png)](https://hackaday.com/wp-content/uploads/2018/08/ds26-tall-front.jpg)

徽章大约 8 英寸高，3 英寸宽，通过一个挂绳孔挂在你的脖子上。是的，今年官方 DEF CON 徽章上有一个标题为[新的附加标准](https://hackaday.io/project/52950-defcon-26-shitty-add-ons)。徽章的体积和重量主要来自嵌套在两个支架中的四节 AA 电池。这是设计中非常有趣的部分，因为电池座贴在微控制器、LED 驱动器和许多 LED 上方的徽章背面。这些发光二极管安装在徽章的下面，通过电路板照亮表面。总共有 30 个这样的发光二极管；有些是 RGB(位于定义图标文本下)，有些是单色。

[![](img/d07101f3a6e18dc4f8a3b5a4dd83c583.png)](https://hackaday.com/wp-content/uploads/2018/08/dc26-under-the-battery-holders.jpg)

主处理器是 PIC32MM0256GPM ，具有 256 kB 和 512 kB SRAM，采用 48 引脚 TQFP 封装，如右图所示。除了驱动徽章，它还提供 USB 连接。左边是另一个目前未知的 48 针芯片。这很可能是一个 LED 驱动器，我们能够阅读的文字类似于“T1918 3236”。如果你对这部分了解更多，请留下评论。

### 神秘组件

 [![PIC12F mystery component](img/6753214cbe113921b803fd8a0e009566.png "DC26 Badge top chip detail")](https://hackaday.com/2018/08/09/first-look-at-def-con-26-official-badge/dc26-top-component-view/) PIC12F mystery component [![Center of board mystery component](img/73fc89acf514bc3c05aace6af3284a61.png "DC26 Badge front silk detail")](https://hackaday.com/2018/08/09/first-look-at-def-con-26-official-badge/dc26-center-of-board/) Center of board mystery component [![6-pin mystery component above the 'D"](img/f385602b175aa78b5f3030c335fd1721.png "dc26-badge-front-thumb")](https://hackaday.com/2018/08/09/first-look-at-def-con-26-official-badge/dc26-badge-front-thumb/) 6-pin mystery component above the ‘D”

电路板顶部附近是一个 8 引脚 SOIC 器件，我最初以为是 EEPROM，但实际上是 PIC12F 微控制器。电路板正面还有两个不同的 6 引脚小器件。一个位于电路板的中心，另一个位于电路板靠近电池座的一侧。

同样，如果你知道这些组件是什么，或者它们的功能，请留下评论。

## 游戏

使用微型 USB 电缆连接到徽章，它会在/dev/ttyACM0 上枚举。连接后，有趣的信息立即可用。

[![](img/12c790b1e518f52eaaa9623985700d29.png)](https://hackaday.com/wp-content/uploads/2018/08/screenshot-from-2018-08-09-10-57-15.png)

制造商在“Tymkrs”中列出，序列号为“D00D 死牛肉饲料 C0ED”。产品 id 被列为“Cyphercon 3.0”，这显然是今年 4 月在密尔沃基举行的活动中的 Cyphercon 徽章的延续。

我刚刚做了一个快速的`cat /dev/ttyACM0`，你会看到一个彩色的界面。底部是一排控件，对应于徽章底部的电容式触摸按钮。

[![](img/d298622737e0a26fcf6dc3791e553838.png)](https://hackaday.com/wp-content/uploads/2018/08/dc26-badge-and-terminal.jpg)

您可以看到终端上的向下箭头和向右箭头是绿色的。这表示从您的当前位置可以进行哪些移动。触摸徽章上的方向是我唯一能找到的导航控制。但我没有使用合适的串行终端，所以可能有更多的功能隐藏在里面。

[![](img/ac2cd17c2f8bf153fb2d2c3e040c1948.png)](https://hackaday.com/wp-content/uploads/2018/08/dc26-badges-connect.jpg)

该游戏在徽章和外壳之间是交互式的，但也在其他徽章之间是交互式的。棋盘底部的连接器提供徽章之间的互动，将徽章正面显示的绿色玩家向下移动一个锁定级别的秘密是将徽章连接到人。我被告知下一级解锁是连接徽章的人到呆子。这是一个令人愉快的互动水平，因为它超级快速和简单，但促进你去寻找所有不同版本的官方徽章。

[![](img/d298622737e0a26fcf6dc3791e553838.png)](https://hackaday.com/wp-content/uploads/2018/08/dc26-badge-and-terminal.jpg)

至于游戏本身，这是一个美味的复古文本游戏。能够在构成徽章表面的地图上跟踪您的进度是非常棒的。每个人都是一个记分牌，理解闪光的善良是一个令人满意的设置，肯定会越来越令人沮丧，你挑战自己在游戏中前进。

棋盘上的这张地图是在 ASCII 艺术中模仿的。上面你可以看到我的绿色玩家站在徽章上一组楼梯的左边。在终端屏幕的右侧寻找同一组楼梯。下面是输出的另一个示例屏幕。

[![](img/f70b818b853321ee1e08f1e806ccfd03.png)](https://hackaday.com/wp-content/uploads/2018/08/dc26-arg-screen.jpg)

## 解开这个徽章！

黑一枚徽章需要一个村子。[点击此魔法链接](https://hackaday.io/project/160333/token/082005aa-c1c9-4424-8b68-fb09ba80ca7d)自动加入 Hackaday.io 上的徽章解决项目，您可以[在此查看项目](https://hackaday.io/project/160333-def-con-26-official-badge-hacking)。

为你试图在徽章上解决的每个挑战创建新的项目日志。进入[公共聊天室](https://hackaday.io/messages/room/274246)讨论正在发生的事情。欢迎所有人，你不需要在这里参加。向手里有徽章的人询问更多信息，并应对想到的挑战！只要确保你尽可能快地发布新信息。