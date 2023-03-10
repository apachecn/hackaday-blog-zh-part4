# 树莓派与一些严重的图形肌肉

> 原文：<https://hackaday.com/2021/09/20/raspberry-pi-with-some-serious-graphical-muscle/>

[Jeff Geerling]定期修补 Raspberry Pi 计算模块，与常规 RPi 4 不同，它包括一个 PCI-e 通道。运气好的话，他能够获得 AMD 镭龙 RX 6700 XT GPU 卡，并且[决定尝试将其插入 Raspberry Pi 4 计算模块](https://www.youtube.com/watch?v=LO7Ip9VbOLY)。

虽然您可能不会使用 setup 之类的工具运行游戏，但有许多独特而有趣的基于计算的工作负载可以卸载到 GPU 上。在类似于在割草机上安装 V8 的情况下，Raspberry Pi 4 可以输出 5-10 瓦，GPU 可以输出 230 瓦。不幸的是，IO 板上的 PCI-e 插槽并没有考虑到高功耗芯片的设计，所以[Jeff]引入了一个成熟的 ATX 电源来为 GPU 供电。为了避免不同接地层的问题，为 Raspberry Pi 设计了一个适配器，它也由 PSU 供电。插卡最初产生了有希望的结果。特别是，Linux 检测到了卡并正确地映射了 bar(基址寄存器)，这在过去对于他使用其他设备来说是个问题。BAR 允许 PCI 设备将其内存映射到 CPU 的内存空间，并跟踪映射内存范围的基址。

AMD 好心为内核提供 Linux 驱动。[Jeff]介绍了内核的交叉编译，并提供了一个很好的 docker 容器，可以快速再现构建的环境。有一个错误阻止了 AMD 驱动程序的编译，所以他不能得到一个完整的内核。自从那段视频之后，他一直在 GitHub 上用一个有趣的话题慢慢地讨论这个问题。从为 Pi 耗尽内存空间到为 GPU 本身进行 PSP 内存训练，什么都遇到过。

勇敢的小计算模块不断扩展的能力对我们 Hackaday 来说是一件美妙的事情，正如我们在今年早些时候看到的[获得 NVMe 启动](https://hackaday.com/2021/03/29/nvme-boot-finally-comes-to-the-pi-compute-module-4/)。我们期待着[Jeff]在 GPU 方面取得的进步。休息后的视频。

 [https://www.youtube.com/embed/LO7Ip9VbOLY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/LO7Ip9VbOLY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

