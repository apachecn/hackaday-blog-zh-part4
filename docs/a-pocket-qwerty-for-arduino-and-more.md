# 适用于 Arduino 和其他产品的袖珍 QWERTY

> 原文：<https://hackaday.com/2019/09/03/a-pocket-qwerty-for-arduino-and-more/>

如果你想给你的 Arduino 项目添加一个键盘，选项是非常有限的。我们在密码保护的门锁项目中都见过红色和蓝色的 4×4 薄膜，手机布局版本也有几乎相同的功能。是不是应该有一个完全兼容 Arduino 的键盘了？[ELECTRONOOBS]是这么认为的。

这个 41 键 Arduino 键盘 PCB 是他下一个项目的垫脚石，一对双向发短信的机器。(这很好，因为我们完全打算这么建议)。它基于无处不在的红/蓝色键盘，但它有一个完整的 QWERTY 布局。还有一个 shift 按钮，可以打开特殊字符和大写字母，添加的 return、ok 和 send 键将它放在顶部。毫无疑问，这款键盘最好的部分是柔软无声的按钮。虽然你用点击反馈来换取舒适，但在几十次按压后，这是非常值得的。

键盘使用板载 ATMega328P 来扫描按钮按压矩阵，对其进行解码，并通过 UART 或 I C 将其发送到 Arduino。[ELECTRONOOBS]目前通过 [Patreon](https://www.patreon.com/ELECTRONOOBS/posts) 提供 PCB 文件，尽管它们将在未来开放。代码已经可以在他的网站上下载了。

未来的计划包括一个 LED 来指示何时按下 shift，并在丝网印刷的数字旁边添加特殊字符(哎呀！).请务必在休息后观看构建视频。

想要一个 Arduino 驱动的键盘来进行更长时间的字母表搜索吗？装上马鞍，骑上这只糖果色的机械独角兽。

 [https://www.youtube.com/embed/M6OcPC5g_eM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/M6OcPC5g_eM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

