# 逆向工程 900 MHz RC 发射机和接收机

> 原文：<https://hackaday.com/2022/02/20/reverse-engineering-a-900-mhz-rc-transmitter-and-receiver/>

对于那些建造自己的遥控设备的人来说，如遥控船和四轴无人机，拥有一个良好的发射器-接收器设置是他们建造的最终可用性的一个重要因素。许多发射机在 2.4 GHz 频段可用，但有些工作在不同的频率，如 868/915 MHz 频段。TBS Crossfire 就是这样一种发射器，由于其远程性能，它已经成为一种流行的型号。

[![The channel hopping sequence of a TBS Crossfire transmitter](img/34700f9e8ca18e2e1f5b0a5d2443ca6a.png)](https://hackaday.com/wp-content/uploads/2022/02/TBS-Crossfire-channel-hopping-sequence.png)

The channel hopping sequence

当[g3gg0]为他的无人机购买交叉火力装置时，他发现接收器模块只不过由 PIC32 微控制器和 SX1272 LoRa 调制解调器组成。这让他开始思考射频协议是否容易解码。事实证明，这并非微不足道，但也并非不可能。首先，他使用 CYC1000 FPGA 板构建了自己的 SPI 嗅探器，以揭示 PIC32 发送给 SX1272 的确切寄存器设置。Crossfire 使用信道跳频，只需查看寄存器设置，就可以很容易地找出跳频序列。

一旦解决了这个问题，下一步就是找出哪些数据通过这些渠道流动。数据包似乎是以一种简单的方式构建的，但它们包含一个未知的 CRC 校验和。幸运的是，暴力破解并不难；校验和最有可能用于防止接收器接收到来自不同发射器的信号。

[g3gg0]的博客文章详细介绍了 Crossfire 的协议以及获取这些信息所需的逆向工程过程。最终的结论是，虽然该协议是高效和健壮的，但它不能提供针对窃听或故意干扰的安全性。当然，对于大多数 RC 应用程序来说，这完全没问题，只要用户意识到这一点。

如果你对解码射频协议感兴趣，你可能还想让[尝试使用逻辑分析仪](https://hackaday.com/2021/09/16/an-rf-remote-is-no-match-for-a-logic-analyser/)。但是如果你只是想复制一个现有的发射器的信号，简单的[欺骗几个按钮](https://hackaday.com/2022/01/31/reusing-proprietary-wireless-sockets-without-wireless-hacking/)可能会更容易。

 [https://www.youtube.com/embed/GCU4Pnw3n-c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/GCU4Pnw3n-c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

