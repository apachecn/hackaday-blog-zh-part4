# 自定义数据包嗅探器是学习 CAN 的好方法

> 原文：<https://hackaday.com/2020/07/02/custom-packet-sniffer-is-a-great-way-to-learn-can/>

[Aaron]在将他汽车中的音响换成更现代的基于 Android 的解决方案时，注意到它只利用了一个 CAN 差分对与汽车进行通信，而不是使用模拟信号的一整束电线。这并不奇怪，因为现代汽车总是使用 CAN 总线在各种外设和传感器之间建立通信。

在一系列视频中， [[Aaron]详细介绍了他如何利用这个机会探索 CAN 通信的一些本质](https://www.youtube.com/watch?v=fj8ZLTubeko&feature=youtu.be)。在第 1 部分中，他使用 Arduino、MCP2515 CAN 控制器和 CAN 总线驱动 IC 设计了一个廉价的定制 CAN 总线嗅探器，演示了这种相对简单的硬件配置如何与开源软件一起使用，以解码一些真实的 CAN 总线流量。[他的系列的第 2 部分](https://www.youtube.com/watch?v=_Ajn560TLIo)围绕着杜平，通过发送正确的 CAN 数据包，他的安卓立体声系统进入各种操作模式。

这些视频是学习与 CAN 的各种抽象层相关的一些基本注意事项的好方法。一旦你覆盖了这些，你就可以做一些非常有趣的事情，比如这些可疑的设备[在你的里程表上拉一个中间人攻击！](https://hackaday.com/2020/03/13/inside-a-can-bus-mileage-manipulator/)同时，我们希望看到关于 CAN 硬件消息过滤和屏蔽的第 3 部分[Aaron]！

 [https://www.youtube.com/embed/fj8ZLTubeko?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/fj8ZLTubeko?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/_Ajn560TLIo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_Ajn560TLIo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

