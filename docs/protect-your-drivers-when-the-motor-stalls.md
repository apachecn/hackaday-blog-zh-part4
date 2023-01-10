# 当发动机熄火时保护你的司机

> 原文：<https://hackaday.com/2022/06/13/protect-your-drivers-when-the-motor-stalls/>

[Mark re host]向我们讲述了一个涉及价值 200 美元的电机驱动硬件过早报废的悲剧事件，并且[分享了一个简单的电路](https://drmrehorst.blogspot.com/2022/05/bank-account-protection-circuit-for.html)，以便我们可以防止将来发生这样的悲剧。他的 [Arrakis 沙盘项目](https://hackaday.io/project/181754-arrakis-sand-table)涉及了相当多的电机，由于忘记了在软件中添加限制，他将一个电机驱动的机械装置猛地放到了桌子的固定部分。电机的反电动势产生了一股能量，摧毁了电机驱动器、控制板和电源。

事后分析完成后，他必须防止这种情况再次发生——最好是在硬件方面。基于 Gecko Drives 的一个小的 [appnote，](https://www.geckodrive.com/support/returned-energy-dump.html)他设计了一个简单的 PCB，只要电流开始流向它不应该流向的方向，它就会用一个大功率电阻分流电机。他深入探讨了电路的工作方式和器件选择背后的原因，展示了 LTSpice 仿真并分享了 PCB 文件。这是他第一次在 KiCad 设计 PCB，我们相信他做得很好！如果你想了解这样的电路是如何工作的，以及构建一个这样的电路需要什么，这篇工作日志当然值得一读。

他称之为“银行账户保护”电路，我们完全可以理解。当然，不仅仅是数控工作台需要这样的保护——我们已经看到[一种针对小型临时电动汽车的解决方案，例如](https://hackaday.com/2019/05/11/battle-tested-current-limiter-for-cheap-dc-motor-controllers/)。然而，发动机的发电特性并不总是一个问题——这里只是一个黑客[试图将它们很好地利用起来的例子。](https://hackaday.com/2012/01/23/investigating-the-generative-properties-of-a-stepper-motor/)

 [https://www.youtube.com/embed/IierWEZ0SKU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/IierWEZ0SKU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



我们感谢[P-Storm]与我们分享这个！