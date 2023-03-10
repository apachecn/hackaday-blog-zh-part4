# USB Type-C 的奇妙世界

> 原文：<https://hackaday.com/2018/08/17/the-wonderful-world-of-usb-type-c/>

尽管 USB-C 在过去几年变得很普遍，但它仍然有点神秘。试着问一个拥有新的刀片式笔记本电脑的人它有什么端口，回答通常会包括一个尴尬的停顿，然后是“USB-C？”。除非你听到“USB 3”或者 USB 3.1。甚至可能是“一个充电口”。那么，你笔记本电脑侧面的那个新椭圆孔叫什么？它到底能做什么？回收实验室的[jason]整理了一系列必读的博客文章，分别是 2016 年的[和 2017 年的](https://www.reclaimerlabs.com/blog/2016/12/31/usb-c-for-engineers-part-1)[关于 USB 3.1 兔子洞的深度](https://www.reclaimerlabs.com/blog/2017/1/12/usb-c-for-engineers-part-2)以及[关于电力传输的](https://www.reclaimerlabs.com/blog/2017/2/1/usb-c-for-engineers-part-3)。哦，他还用它做了一个光滑的简易烤箱。

![](img/4647f2ec6a2c87da973992e986f1399b.png)

A single USB Type-C connector

说到 USB-C，从头说起很重要。“USB-C”这几个字意味着什么？不出所料，答案很复杂。“USB Type-C”仅指物理连接器及其使用细节，包括它包含的 24 个引脚中的一些。然后还有其他的条款。“USB 3.1”是包含 Type-C 连接器和新的高速数据总线(“USB SuperSpeed”和“SuperSpeedPlus”)的总体标准。此外，还有“USB 电源传输”,它描述了电源模式，甚至更多的引脚分配。我们在这里总结，所以去阅读更多细节的第一篇文章。

第二篇文章用了 1200 字来概述 USB 3.1 的电气规格、配置通信和连接器类型。

![A GIF of a flipping USB Type C connector](img/0a042fbf5504080cc8d8dbd737aade4a.png)

Marketing at its finest

第三篇文章是关于 USB 供电的。功率传输不仅包括支持的新的更高功率模式(高达 100 瓦！)，而是使用 Type-C 连接器上可用的额外 10 或 13 个引脚的方法。这是 USB-C 的好处和坏处，允许表面上相同的端口传输常见信号，如 HDMI 或 DisplayPort，充当模拟音频输出，并提供更多奇特的接口，如 PCIe 3.0(以雷电 3 的形式，这是该连接器可以使用的另一个功能)。

在这一点上应该很清楚,“USB Type-C”所涉及的主题异常复杂。省去 90MB 规格压缩文件的麻烦，浏览一下[jason]的帖子，了解发生了什么。为了获得关于电力输送的更多细节，他在[的另一篇文章](https://www.reclaimerlabs.com/blog/2017/5/16/example-usb-power-delivery)中浏览了样本交易。