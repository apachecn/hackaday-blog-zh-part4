# 离散逻辑 UART 保持 8 位 TTL 计算机连接

> 原文：<https://hackaday.com/2020/08/26/discrete-logic-uart-keeps-8-bit-ttl-computer-connected/>

可怜的 TTL 电脑爱好者。这是一种痴迷，真的——使用离散逻辑芯片来构建一台在性能方面可能比不上 80 年代 8 位机的计算机。然而，他们仍然带着装满芯片和电线的试验板稳步前进。仔细想想真的挺好看的。

[Duncan]在 Shepherding Electrons 公司，他发现了 TTL 错误，并在建造他的 8 位机器时为它配备了这个离散逻辑 UART。通用异步收发器是如此有用，以至于自 20 世纪 70 年代初以来，这种设备的单片版本就已问世。[Duncan]的版本使串行通信的魔力发生在仅仅 12 个芯片上，全部来自 74LS 逻辑系列。

似乎建造一个分立逻辑 UART 的壮举还不够，【Duncan】在没有示波器的帮助下完成了这件事。调试就是用一个简单的 1 Hz 555 定时器电路代替 2.4576 MHz 晶体振荡器时钟；时钟速度的降低使得用 led 检查电压和监控线路状态变得更加容易。一旦电路工作，全速时钟被替换回来，使他能够以高达 38，400 bps 的速度与他的 8 位计算机对话。颜色让我们印象深刻。

要了解更多 TTL 计算机的优点，并了解[Duncan]从哪里获得的灵感，请查看[Ben Eater]的许多离散逻辑项目——他白手起家的 6502，[低端显卡](https://hackaday.com/2019/07/07/low-res-video-card-is-still-amazing-since-its-made-out-of-logic-chips/)，甚至[他的串行通信](https://hackaday.com/2018/06/14/a-crash-course-on-reliable-communication/)。