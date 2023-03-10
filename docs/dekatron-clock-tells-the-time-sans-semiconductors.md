# 德卡龙时钟显示时间，无半导体

> 原文：<https://hackaday.com/2022/12/05/dekatron-clock-tells-the-time-sans-semiconductors/>

多年来，有几种内存和显示技术在一段时间内服务于某个特定的领域，但当更合适的技术出现时，它们被取代并被遗忘。其中之一是迪卡龙:一种组合记忆和显示管，在 20 世纪 50 年代和 60 年代有所应用，但很快就过时了。然而，正如[grobinson6000]在他的 Dekaclock 项目中展示的[，它们的复古设计和组合内存/显示功能使它们成为当今时钟黑客的优秀组件。](https://www.youtube.com/watch?v=hG6PmNYgzMA)

迪卡龙管基本上是一种氖管，十个阴极排成一圈。在任何时候，只有一个阴极被点亮，你可以通过向它的管脚施加脉冲来使显像管跳到下一个阴极。Dekaclock 使用 50 赫兹的电源频率在一个电子管中产生 20 毫秒的脉冲；当它达到 100 毫秒时，它触发下一个计数数百毫秒的电子管，这又触发另一个计数秒的电子管，以此类推，以分钟和小时为单位。

Dekaclock 完全不使用半导体:整个系统由玻璃管和无源元件构成。然而，[grobinson6000]还建立了一个辅助系统，充满了半导体，使时钟更容易使用。它位于 Dekaclock 的顶部，使用 GPS 接收器自动设置正确的时间。它还可以记录十进制计时器显示的时间，并告诉您它们已经偏离初始设置多远。

这两个系统都装在光滑的木箱中，完全符合管子的复古美学。[grobinson6000]在观看了我们之前介绍的另一款 dekatron 时钟后，受到了制作 Dekaclock 的启发，并设计了与其配合使用的 GPS 接收器。迪卡侬是令人惊讶的多功能设备:你可以用它制作任何东西，从[网络速度计](https://hackaday.com/2015/07/30/an-internet-speedometer-with-a-dekatron/)到[厨房定时器](https://hackaday.com/2009/04/06/dekatron-kitchen-timer/)。

 [https://www.youtube.com/embed/hG6PmNYgzMA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/hG6PmNYgzMA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

