# Python 复活了点阵打印

> 原文：<https://hackaday.com/2018/08/09/python-resurrects-dot-matrix-printing/>

如今，打印机——尤其是家用打印机——很可能会从喷嘴喷出墨水。越来越难找到家用激光打印机，点阵等早期的打印机技术几乎已经从人们的家中消失，即使你仍会在一些办公室看到一些打印多部分表格。

[Thomas Winningham]在一家快餐店的停车场花 20 美元买了一台旧的 Commodore 点阵打印机。让它工作起来会有多难？确实有多难。看看下面的视频，看看整个冒险。打印机背后的原理很简单。头部有一排或两排针，每排由一个螺线管控制。磁头在纸面上移动，你的工作——如果你决定接受的话——就是把针推到正确的位置。像打字机一样的墨带使用——哦，是的，更多的消失技术——将墨水留在纸张上被针穿透的地方。

你通常不会考虑所有这些，因为打印机的固件会处理所有事情。但是这么老的打印机有很多问题，包括 Commodore 古怪的类似 ASCII 的标准。尽管如此,[Thomas]还是做了出色的工作，并且能够完成:

*   使用 GIMP、ImageMagick 和枕头进行抖动
*   将打印机引脚映射到 NumPy 矩阵
*   使用 Tea4CUPS 将 Python 与 CUPS 集成
*   使用 NumPy 和 Read-Font 库定制字体(移植到 Python 3)

这将教会他在快餐店的停车场买东西。

顺便说一下，如果你有耐心，[你只需要一个 pin 码](https://hackaday.com/2007/04/11/one-pin-diy-dot-matrix-printer/)就可以从 Commodore 或任何电脑上打印。就像其他制造噪音的东西一样，有人[也将尝试用点阵打印机制作音乐](https://hackaday.com/2014/02/20/eye-of-the-tiger-as-played-by-a-dot-matrix-printer/)。

 [https://www.youtube.com/embed/45aeGWPRL0g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/45aeGWPRL0g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

