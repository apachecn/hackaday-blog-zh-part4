# 机电 YouTube 子计数器用点击换点击

> 原文：<https://hackaday.com/2019/04/28/electromechanical-youtube-sub-counter-trades-clicks-for-clacks/>

获得一个新的 YouTube 用户是一件好事，比电话通知更值得大肆宣扬。但也许闪光灯真的不再适合你了，或者你只是喜欢声音上的安慰而不是视觉上的。嗯，还有什么比机电 7 段显示器清脆的*咔嗒声*更令人满意的呢？[他们六个，当然是](https://www.youtube.com/watch?v=zKdXMAyXzMI)。这些东西看起来很棒，听起来也很棒，一旦设置好，它们就不需要电源来保持这种状态。

这些显示器通过反转流经电磁铁的电流在黑白之间切换，所以[Zack]转向 H 桥以便和 DC 一起使用它们。不过，六个显示器的每一个部分都有一个 H 桥，累加起来很快。为了解决这个问题，[Zack]将每个电磁体的一个电极绑在一起用于公共信号输入，并使用另一个电极单独控制每个部分。然后，他能够将所有的 A 段、所有的 B 段等等连接在一起，并且只需要 13 个 H 桥来完成这一切。

只有一件事[扎克]没有料到。一旦他把电路板焊接好并开始运行，显示器就开始变得奇怪。线圈的低阻抗导致它们在公共路径上相互影响，所以他增加了二极管阵列来保持它们在一条线上。

[Zack]正在使用一个 ESP32 通过 Google API 获取 411，并使用四个八路串行开关来驱动显示器。比所有这些*咔嗒声*更令人满意的是，显示器的操作经济性融入了[Zack]的代码中——当它们向上计数时，第一个数字和下一个数字共有的任何段都保持不变。增加您的方式过去休息，以检查建立视频。

不注重数字，但仍想庆祝每一个新的潜艇？试试跳舞机器人或 T2 俄罗斯方块麻花游戏。

 [https://www.youtube.com/embed/zKdXMAyXzMI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/zKdXMAyXzMI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

