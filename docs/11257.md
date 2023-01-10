# 任天堂 DSi 启动 rom 的 EM 故障

> 原文：<https://hackaday.com/2021/09/11/em-glitching-for-nintendo-dsi-boot-roms/>

一些黑客事件是在遥远的田野里泥泞和尘土飞扬的事情，另一些发生在黑暗的大厅里，但我去了一个可以作为在一个充满文化和历史的欧洲城市的豪华休息体验的事件。《新线》的故事发生在比利时同名城市 Hackerspace Gent，上周末我去那里感受了那里的氛围，以及讲座和研讨会的日程安排。其中一个良好的开端是由[PoroCYon]，[提出的，他对从任天堂 DSi 中恢复启动 rom 所涉及的故障技术](https://www.youtube.com/watch?v=l0eCcwRNS1s)的精彩介绍教会了我们许多以前从未见过的东西。

你将在休息时间下面看到的演讲开始于描述故障的过程——使用电源干扰来中断微处理器的操作并避免某些指令——以绕过安全代码。然后，它转移到各代任天堂游戏机和手持设备中使用的一些保护机制，然后转移到 DSi 上的工作，在这一点上，谈话转移到一个领域，这可能是故障界的旧帽子，但对我来说是新的；电磁干扰。

EM 毛刺涉及使用一个小线圈来产生精确定时的电磁脉冲，从而在芯片中感应毛刺电压。令人着迷的是，EM 探针可以做得足够小，以针对芯片的单个区域，因此使用它需要一种蛮力技术，将探针固定在计算机控制的 X-Y 底座上，尝试所有的时间和位置组合。

DSi 板上有两个处理器，这在 ARM7 上取得了成功，但其同伴 ARM9 尚未开发。有一组很有希望的攻击向量可供尝试，其中 ARM7 将 ARM9 置于可以中断的状态似乎是最有希望的。很明显，这个季度还会有更多的收入。

演讲的更多细节可以在这个知识库中找到[，对于那些对 EM 故障感兴趣的人，你可以在这个视频](https://git.titandemo.org/PoroCYon/nl21brom)和这个项目中找到更多的[用它来攻击](https://www.youtube.com/watch?v=DuP7TsqDr1M)[一个壁虎微控制器](https://limitedresults.com/2021/06/enter-the-efm32-gecko/)。

 [https://www.youtube.com/embed/l0eCcwRNS1s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/l0eCcwRNS1s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

