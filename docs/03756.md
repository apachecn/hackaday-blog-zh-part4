# 苹果闪电视频适配器运行 IOS，动态加载

> 原文：<https://hackaday.com/2019/07/30/apple-lightning-video-adaptors-run-ios-dynamically-loaded/>

很长一段时间以来，苹果一直是一家在外设方面独辟蹊径的公司，昂贵的专有硬件是其连续几代产品的主流。它目前的专有接口系列之一是 Lightning 连接器，最好被认为是苹果专用的，与世界其他地方的 USB-C 概念相同。有一大堆白色危险的外设可以挂在你的 iDevice 的 Lightning 端口上，包括一对显示适配器，允许它们驱动 HDMI 或 VGA 显示器。[Lisa Braun]已经对一个失败的外设进行了拆解，她的分析让我们对苹果创造外设的方式有了一些了解。

你可能会认为它们主要包含相当于显卡的功能，但事实上，它们拥有自己的成熟 SoC，运行自己的操作系统，使用相同的达尔文内核作为主机。出乎意料的是，这并不保存在适配器本身上，而是随 iOS 一起提供并动态加载。因此，包含它的文件可以从 iOS 中检索并解压缩，从而导致一些有趣的分析。对于我们这些不习惯 Lightning 内部结构的人来说，有趣的是，据透露，该设备可以通过适当的拼凑适配器从 USB 端口驱动，允许全尺寸 MacOS 设备询问它。这对于记性好的读者来说可能不是什么新闻，不过我们过去已经告诉过你关于对 Lightning 连接器的[逆向工程。](https://hackaday.com/2015/02/14/reverse-engineering-apples-lightning-connector/)