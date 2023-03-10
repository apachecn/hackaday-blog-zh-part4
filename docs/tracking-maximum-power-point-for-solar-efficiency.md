# 跟踪太阳能效率的最大功率点

> 原文：<https://hackaday.com/2021/09/19/tracking-maximum-power-point-for-solar-efficiency/>

在过去太阳能电池板并不便宜的时候，许多人(甚至是大型能源公司)使用太阳能跟踪器来确保他们的电池板总是物理地指向太阳，以确保他们尽可能收获每瓦特的能量。然而，由于太阳能电池板的价格暴跌，安装复杂的机器来跟踪太阳已经不经济了。但是所有的太阳能发电场仍然跟踪其他东西，称为最大功率点(MPP)，它确保即使是固定的电池板也能优化发电。

虽然小型 MPP 追踪器(MPPT)在 200 美元范围内的太阳能充电控制器中可用，非常适合小型离网设置，[【ASCAS】又名【TechBuilder】决定推出价格低得多的开源版本](https://www.instructables.com/DIY-1kW-MPPT-Solar-Charge-Controller/)，因为这些单元的大部分成本都在研发中&而不是实际的组件本身。为此，他在 MPPT 中使用的方法与任何商用设备基本相同，即所谓的同步降压转换。这使用了特别配置的开关模式电源(SMPS ),以便在任何给定的条件下非常快速地将面板的功率输出匹配到最佳功率点。它甚至可以在许多不同的电池配置和化学物质上工作，所有这些都可以通过软件进行配置。

这个构建非常广泛，深入到电气理论和设计选择中。值得注意的一个设计选择是使用 ESP32 而不是 Arduino，因为在进行模数转换时可以获得更高的分辨率。甚至还有一个关于电感核心设计的冗长讲座，当然这个项目的所有内容都是开源的。我们也看到了在 T1 之前，ESP32 和 MPPT 一起工作，虽然稍微不那么精致，但仍然很有趣。

感谢[Sofia]的提示！

 [https://www.youtube.com/embed/ShXNJM6uHLM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ShXNJM6uHLM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

