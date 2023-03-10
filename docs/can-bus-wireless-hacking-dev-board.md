# CAN 总线无线接入/开发板

> 原文：<https://hackaday.com/2021/07/11/can-bus-wireless-hacking-dev-board/>

[Voltlog]已经在他的大众高尔夫的 CAN 总线控制台上干了很长时间了。据推测，对于他的项目，可用的 CAN 总线接口板在某些方面有所欠缺，无论是技术上还是价格上。于是【volt log】[设计了自己的无线 CAN 总线黑客攻击开发模块，名为 ESP32 CanLite](https://www.youtube.com/watch?v=DLKQcw506ck) (见破下方视频)。该板是为满足他的项目需求而定制的，他声称这不是一个通用工具。尽管如此，我们认为许多人会发现他为这个模块选择的特性也非常适合他们的项目。

在他的设计介绍中，他讲述了他所面临的各种设计决策。正如项目名称所示，他使用 ESP32 作为主控制器，因为它的无线无线电和内置 CAN 控制器。该板由汽车的+12V 电源供电，因此它使用宽输入范围(4 至 40 V)的开关稳压器。他增加的一个功能是使用 ST VN750PC 切换汽车配件的能力，ST VN 750 PC 是一个漂亮的高端驱动器，采用 SO-8 封装，集成了安全措施。

该项目以开源形式发布，文件可以从他的 [GitHub 库](https://github.com/voltlog/CanLite)中提取。我们注意到原理图上标有 VOLTLINK 的调试连接器，并发现[对这个定制接口](https://www.voltlog.com/voltlink-a-fancy-usb-serial-adapter-esp32-programmer-voltlog-356/)的描述很有趣。基本上，他对市场上各种 USB 转串行适配器的质量和性能不满意，决定自己制作。这可能是[Voltlog]项目中的一个共同主题吗？

如果您想自己构建 ESP32 CanLite，请注意一点。虽然[Voltlog]在项目开始时有意选择了常见且易于购买的部件，但由于全球部件短缺问题，几个关键芯片最近几乎不可能获得(在他的 Tindie 页面上甚至[缺货)。](https://www.tindie.com/products/voltlog/canlite-esp32-can-development-board/)

如果你想更深入地了解 CAN 总线黑客攻击，请查看我们在 2016 年写的[这篇演讲。你有什么喜欢的 CAN 总线开发板和/或工具吗？请在下面的评论中告诉我们。](https://hackaday.com/2016/07/27/yes-you-should-be-hacking-your-cars-data-system/)

 [https://www.youtube.com/embed/DLKQcw506ck?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/DLKQcw506ck?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

