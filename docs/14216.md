# Stratum 1 特级时间服务器的预算

> 原文：<https://hackaday.com/2022/07/15/stratum-1-grandmaster-time-server-on-a-budget/>

[Jeff Geerling]跟踪各种开源时间项目已经有一段时间了，[终于能够在您当地的实验室](https://www.youtube.com/watch?v=RvnG-ywF6_s)展示一个可行且负担得起的纳秒级精确计时解决方案。早在 2020 年 10 月，随着 Raspberry Pi CM4 计算模块的推出，低成本时间服务器成为可能，其 Broadcom 网络芯片(BCM54210PE)支持 PTP(精确时间协议，IEEE-1588) 1PPS 输出和基于硬件的时间戳。尽管 CM4 数据表指定了 PTP 支持，但它在内核中不可用。去年二月提出了一个[问题](https://github.com/raspberrypi/linux/issues/4151)，这个月终于发布了树莓 Pi 内核支持。

[Jeff]在休息时间下面的视频中演示了让两个 CM4 模块在几十纳秒内同步是多么容易。仅此一点在许多项目中就非常有用。但是如果你想要真正稳定和绝对的时间，你需要一个 stratum 1 外部源。这些时间服务器在 PTP 术语中被称为“大师”,传统上是价值数万美元的专用套件，使用精密振荡器实现稳定性，并使用来自导航卫星或地面广播站等 stratum 0 设备的 RF 信号来获得绝对时间。但是正如从事内核更新工作的 Lasse Johnsen 在视频中所说:

> 到 2022 年，这些来自传统供应商的专门制造的特级大师时钟就像 1998 年的 Raq 和 Qube 等网络服务器一样重要。

现在，您可以在自己的实验室中从开源项目中构建自己的低成本 stratum 1 时间服务器。视频中显示了两个例子。[开放时间服务器](https://github.com/opencomputeproject/Time-Appliance-Project/tree/master/Open-Time-Server/)项目的工时记录卡使用 GNSS 卫星接收器和微芯片 MAC-SA5X 铷振荡器。如果这对你的项目或预算来说是多余的，那么 [Time4Pi CM4 hat](https://store.timebeat.app/products/gnss-raspberry-pi-cm4-module) 将会以低于 200 美元的价格发布。如果准确的时间保持是你的事情，这项技术现在是普通家庭实验室可以达到的。你也可以在非 CM4 的树莓派中加入 PTP——看看我们去年报道过的[实时帽子](https://hackaday.com/2021/08/16/new-part-day-raspberry-pi-hat-for-ieee1588-precision-time-protocol/)。

 [https://www.youtube.com/embed/RvnG-ywF6_s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/RvnG-ywF6_s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/tU0xC1ynaT8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/tU0xC1ynaT8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

