# 欺骗智能仪表在工作台上工作

> 原文：<https://hackaday.com/2022/03/31/tricking-a-smart-meter-into-working-on-the-bench/>

当你正在使用的小工具由电池或 USB 充电器供电时，在工作台上运行它可能是相当安全的。但是，当你的逆向工程目标是住宅电表时，事情就有点冒险了。

并不是说这种升高的危险等级阻止了[Hash]探索智能电表带来的奥秘。尽管如此，出于让事情更安全一点的愿望，他想出了一个在工作台上给电表安全供电的巧妙方法。[Hash]发现，电表背板上的内部开关式电源很容易通过 12 伏台式电源进行反馈，而不是像通常插入电表底座时那样为电表提供 240 伏的交流电源(这些电表面向北美市场，在那里，分相 240 伏是住宅连接的标准。)但这对血糖仪来说还不够——它通电了，但仍处于复位状态，没有完全启动。还需要更多的东西才能让这款仪表充满活力。

那个东西被证明是一个小的交流信号。正常情况下，电阻网络将 240 伏的电源分压至约 3 伏，供仪表中的传感电路使用。[Hash]发现，将一个 60Hz、600mV、DC 偏置约为 3 伏的正弦波信号注入检测电路，足以欺骗电表，让它认为自己插入了电表底座。下面的视频有一个黑客的演练，和一些他一直在工作的仪表内部的好镜头。

[哈希]已经使用这些仪表有一段时间了，他学到的一些东西是纯金的。请务必查看[他 2021 年关于电表黑客的 Remoticon 演讲](https://hackaday.com/2022/01/13/remoticon-2021-hash-salehi-outsmarts-his-smart-meter/)中所有精彩的细节。

 [https://www.youtube.com/embed/-saaJrKSkio?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-saaJrKSkio?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

