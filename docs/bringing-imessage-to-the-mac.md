# 将 IMessage 引入 Mac

> 原文：<https://hackaday.com/2022/03/04/bringing-imessage-to-the-mac/>

如果你投资了苹果生态系统，iMessage 的乐趣可能会照亮你的生活。你的手机、台式机和笔记本电脑都会同步你的信息。但是如果你的台式机运行的是 Mac OS 9 或者 System 2 呢？这就是[CamHenlin 的] [MessagesForMacintosh 进入](https://github.com/CamHenlin/MessagesForMacintosh)的原因。

不幸的是，它确实需要更现代的 Mac 来充当更广泛的 iMessage 网络的接入点。现代 Mac 建立了一个可以访问的 GraphQL 数据库。然后，一条串行电缆将您的“retro daily driver”连接到一个转换层，该转换层将串行命令转换为 GraphQL 命令。这可能是一些简单的网络连接的东西，如 ESP32 或在 iMessage Mac 上运行的程序。[CamHenlin]在他的演示中有第二台 Mac mini，见上图。

[CamHenlin]利用他的库协处理器 JS。它允许旧机器将复杂的工作负载移交给更现代的机器，允许现代机器充当协处理器。让一个二进制文件在许多不同版本的 Mac OS 和系统上运行是一件棘手的事情，需要一些技巧。 [Retro68 是一款针对 PowerPC 和 68k 架构的 C++17 编译器](https://github.com/autc04/Retro68)。此外， [Nuklear Quickdraw](https://github.com/CamHenlin/nuklear-quickdraw) 用于以一种高性能的方式提供一个 GUI。

经常在一些现代硬件的帮助下，看老硬件玩新把戏总是一件令人愉快的事。将你的 Mac 连接到互联网就像 Pi T1 一样简单。