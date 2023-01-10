# 使用自制线圈测量电源电流，接受断路器挑战

> 原文：<https://hackaday.com/2021/09/12/using-homebrew-coils-measure-mains-current-and-taking-the-circuit-breaker-challenge/>

像许多黑客一样，[马蒂亚斯·万德尔]喜欢测量他周围的世界，量化他家里发生的事情是一种爱好。因此，当需要检测他家电线中的电流时，他做了我们任何人都会做的事情:[他建立了自己的电流检测系统](https://www.youtube.com/watch?v=P47pjVyPP3w)。

你说什么？任何一个正常的黑客都会买一个瓦特计之类的东西，或者甚至使用市场上可以买到的电流互感器？也许吧，但那就不算是黑客了，不是吗？[Matthias]选择推出自己的传感器有相当实际的原因:商用电表没有足够的响应时间来捕捉他感兴趣的启动尖峰，钳形电流互感器需要将大多数住宅布线中使用的非金属电缆的护套分开，这样做往往会违反建筑法规。因此，他的传感器只是形状适合纳米电缆外部的线圈，经过一点滤波，在许多开关模式电源的高噪声环境中提供更清晰的信号。

通过 ADC 板输入到 Raspberry Pi 中，[马提亚斯]的传感器系统在捕捉商店中一些工具的启动潮方面表现惊人。这就引出了下面视频中有趣的“断路器挑战”部分，我们从中了解到在 15 安培的分支电路上打开断路器到底需要什么。剧透提示:很多。

说到保持电源电流安全，我们之前已经讨论了一点关于电路保护如何工作的。如果你需要[深入了解断路器](https://hackaday.com/2021/01/26/how-does-a-circuit-breaker-break/)，我们也有。

 [https://www.youtube.com/embed/P47pjVyPP3w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/P47pjVyPP3w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢 tip-line stalbar[bald power]的提示。