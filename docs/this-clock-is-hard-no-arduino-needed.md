# 这个时钟很难:不需要 Arduino

> 原文：<https://hackaday.com/2018/07/29/this-clock-is-hard-no-arduino-needed/>

你总是听到人们谈论天气。但是在我们看来，我们看到的时钟比气象站还多。一个恰当的例子是用旧硬盘制成的[frank _ scholl]时钟。我们发现这个时钟根本没有微控制器，这很有趣。定制 PCB 是全数字的，使用线路频率驱动计数器，进而驱动电机。

一个问题是，你必须有一个硬盘驱动器，使用一个非常特殊的电机方案来工作。盘片旋转显示小时，磁头的磁道位置从 0 到 59 计数分钟。两个按钮可以加速旋转，以便设置时钟。你可以在下面的视频中看到这一切。

原理图有点难懂，因为它没有使用传统的逻辑符号，但你可能会弄明白。显然，对于 60 Hz，它需要一点调整，并且您的电机连接不太可能相同。

即使你找不到符合要求的硬盘，用一些马达改装一个现代硬盘也很容易。尽管逻辑电路很酷，但我们也会尝试用微处理器来做这件事。

我们喜欢看到科技发明被这样重新利用。例如，我们见过用米制成的[钟。在](https://hackaday.com/2018/06/22/analog-meters-become-a-clock-for-fathers-day/)之前，我们实际上看到了与此非常相似的[，但它确实使用了 CPU。](https://hackaday.com/2013/11/23/atmega16-hard-disk-clock/)

 [https://www.youtube.com/embed/7EWCB7aaX5s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/7EWCB7aaX5s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

