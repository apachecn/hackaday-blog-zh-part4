# 玩一局万用表

> 原文：<https://hackaday.com/2020/09/05/play-a-game-of-multimeter/>

有许多不同的单板计算机是通用的，但还有另一种针对特定应用。一个这样的例子是 Clockworkpi，一个掌上游戏机风格的游戏控制台，它可能是针对游戏玩家的，但也有同样多的能力做所有常见的 SBC 事情。这是[UncannyFlanigan]通过把时钟工作指针变成万用表所展示的。它也不仅仅是一个简单的数字万用表，它可以显示图形和瞬时读数。

它的核心是一个 Arduino 板，提供模数转换，两个板之间用光耦合器隔离。一个简单的三路开关选择电压、电流和电阻范围，ClockworkPi 接口用 Python 编写。我们可以看到，使用 Arduino 的能力可以很容易地扩展这一点，以提供更多的功能，为此[所有代码都可以在 GitHub 库](https://github.com/liamHowatt/Gameshell-Multimeter)中方便地获得。它还不是一个完美的万用表，因为它缺乏足够的输入保护，但它显示了很大的前景。

如果你对这个项目感兴趣，那么也许你会很高兴地知道[这不是我们展示的第一个国产万用表](https://hackaday.com/2014/04/24/diy-multimeter-arduino-sold-seperately/)。