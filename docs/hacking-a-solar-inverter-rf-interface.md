# 黑进太阳能逆变器射频接口

> 原文：<https://hackaday.com/2021/06/04/hacking-a-solar-inverter-rf-interface/>

廉价无线模块的主要优势之一是它们可以用于消费电子产品，所以如果你知道正在使用什么，你就可以构建自己的兼容硬件。在研究一系列廉价“智能”太阳能逆变器中使用的 RF 接口时[Aaron Christophel]，创建了一个[Arduino 库，使用一个 2 美元的 RF 模块](https://github.com/atc1441/NETSGPClient/tree/development)接收逆变器遥测。休息后看演示。

[Aaron]购买了逆变器和价值约 40 欧元的 USB“数据盒”,该数据盒允许用户无线监控逆变器的状态。打开两个单元后，他发现它们使用 LC12S 2.4Ghz 模块，这可以创建无线 UART 链接。通过一点逆向工程，他能够计算出射频模块的设置和请求逆变器状态所需的串行命令。他没有深入研究可能的安全隐患，但链接中似乎没有任何形式的加密。任何有模块的人都可以嗅探消息，提取逆变器的 ID，并劫持链接。仅仅知道逆变器的状态应该没有那么危险，但是他没有提到还有什么其他命令可以发送到模块。任何其他可能有更严重的影响。

嗅探我们周围空气中闪烁的无线信号是 Hackaday 上的一个常见话题。从用 ESP32 测试 WiFi 网络的安全性到用 SDR 监控 SpaceX 发射的 T2，可能性是无限的。

 [https://www.youtube.com/embed/uA2eMhF7RCY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/uA2eMhF7RCY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

