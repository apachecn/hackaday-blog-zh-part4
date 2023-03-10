# 借助 Luos，快速嵌入式部署得以简化

> 原文：<https://hackaday.com/2021/10/10/with-luos-rapid-embedded-deployment-is-simplified/>

与那些为桌面或移动平台编写固件的人相比，我们这些负责为嵌入式系统开发固件的人有相当多的障碍要跨越。诸如代码重用或可移植性等已解决的问题更难解决。我们怀着极大的兴趣了解了另一种硬件抽象方法，称为 Luos，它将自己描述为嵌入式系统的微服务。

这个开源项目支持由协作微服务组成的分布式架构的部署。通过容器化应用程序和硬件驱动程序，各种组件的接口隐藏在一致的 API 后面。资源位于何处并不重要，多个服务可能运行在同一个微控制器上，也可能运行在不同的微控制器上，但它们可以以相同的方式进行通信。

通过遵循[硬件](https://www.luos.io/docs/hardware-consideration/)和[软件](https://www.luos.io/docs/luos-technology/basics)的设计规则，有可能创建一个协作计算单元的架构，它完全不依赖于实际的硬件。微控制器用一对双向信号在硬件层面对话，所以硬件成本非常低。它甚至与 ROS 集成在一起，因此制造机器人更加容易。

[![](img/d8a668e3e48dbd277ebf83a42eeda579.png)](https://hackaday.com/wp-content/uploads/2021/10/luos_detail.png)

Luos architecture

通过集成一个称为[门](https://www.luos.io/docs/tools/gate)的特殊模块，可以通过 USB、WiFi 或串行端口从主机实时连接到架构，并输出数据流、输入数据或部署新软件。主机软件栈基于 [Python，运行在我们绝对喜欢的 Jupyter 笔记本](https://www.luos.io/docs/tools/pyluos)下。

当前的[兼容性](https://github.com/Luos-io/luos_engine)是与许多 STM32 和 ATSAM21 micros 兼容，所以你很有可能可以将它与你身边的任何东西一起使用，但未来将会有更多的平台。

现在，是的，我们知道了 [CMSIS](https://hackaday.com/2021/03/18/getting-started-with-freertos-and-chibios/) ，以及将硬件抽象层(HALs)用作特定于平台的软件包的一部分的想法，这并不新鲜。但是，不同的平台工作方式大不相同，将代码从一个平台移植到另一个平台，仅仅因为[你不能再得到你更喜欢的微控制器](https://hackaday.com/2021/01/18/pandemic-chip-shortages-are-shutting-down-automotive-production/)，这是一个我们都可以不需要的真正拖累，所以为什么不去克隆 [GitHub](https://github.com/Luos-io/luos_engine) 自己看看呢？

 [https://www.youtube.com/embed/ujh0xNE3TZ8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ujh0xNE3TZ8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

