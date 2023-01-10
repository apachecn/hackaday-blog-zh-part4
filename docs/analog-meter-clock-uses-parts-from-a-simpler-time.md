# 模拟仪表时钟使用更简单时代的零件

> 原文：<https://hackaday.com/2019/12/29/analog-meter-clock-uses-parts-from-a-simpler-time/>

指针转动的时钟对普通人来说很好，但黑客类型更喜欢不同的东西。[Sjm4306]就是这样一个人，[开发了这款模拟表盘时钟，用现代标准来看，我们几乎会认为它是复古的。](https://hackaday.io/project/168974-analog-meter-clock)

构建的核心微控制器是 PIC16F886。微芯片品牌的 8 位微处理器，它没有 Arduino 引导程序或 USB 接口，通过专用程序员进行闪存。它与 DS1302 实时时钟和 MCP4922 DAC 结合使用，前者用于保持精确时间，后者负责产生驱动表盘的输出。表盘本身来自易贝，是简单的电压表。它们有一个新的背衬来显示小时和分钟，而不是伏特，并带有 led 背光。

在这个时代，我们更习惯于看到高端微处理器与集成 DAC 和 USB 编程一起使用，但很高兴看到过去的部分也被使用。[这也不是我们从【sjm4306】上看到的第一个时钟](https://hackaday.com/2019/09/26/mini-vfd-clock-floats-the-display-above-it-all/)。休息后的视频。

 [https://www.youtube.com/embed/UMGQxw7SuRU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/UMGQxw7SuRU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/2SFkq_Ya1xo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/2SFkq_Ya1xo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

