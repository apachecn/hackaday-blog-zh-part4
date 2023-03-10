# 课堂小工具兼容 Arduino

> 原文：<https://hackaday.com/2018/07/22/classroom-gadget-turned-arduino-compatible/>

廉价的二手硬件通常是黑客的沃土，从这个项目来看，几年前风靡一时的数字课堂教具也不例外。[is0-mick]写信告诉我们他是如何设法将这些设备中的一个——智能响应 XE——黑进兼容 Arduboy 的游戏系统的。事实证明，这个特殊的小工具是由 ATmega128RFA 供电的，它本质上是一个 Arduino 兼容的 AVR 微控制器，外加一个 2.4GHz 的 RF 收发器。这使得它成为一个*非常*有趣的黑客平台，特别是因为他们在易贝只卖 3 美元。

[![](img/c2f3239fd24362a1a9fc41ad4623ccc9.png)](https://hackaday.com/wp-content/uploads/2018/07/smartxe_detail.jpg)SMART Response XE 没有内置 USB 串行转换器，所以你需要提供自己的外部编程器来刷新设备。但幸运的是，电路板上有一个带标签的 ISP 连接器，这使得连接一切变得非常简单。

当然，让硬件工作比仅仅在上面闪现一个 Arduino 草图要稍微复杂一些。[is0-mick]已经提供了他的引导加载程序和修改后的库，以使设备的 QWERTY 键盘和 ST7586S 控制的 384×160 LCD 工作。

玩游戏很有趣，但当他的朋友[en4rab]给他发送 SMART Response XE 进行摆弄时，目标实际上是[将它们变成廉价的 2.4 GHz 分析器，类似于 IM-ME](https://hackaday.com/2010/10/09/pulling-data-from-the-im-me-spectrum-analyzer/) 所做的事情。看起来他们进展顺利，[is0-mick]邀请任何有兴趣填补射频方面空白的人参与进来。

 [https://www.youtube.com/embed/6VqPGFtIT8Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/6VqPGFtIT8Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

