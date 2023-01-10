# 带数据记录的定制虚拟负载

> 原文：<https://hackaday.com/2021/03/15/custom-dummy-load-with-data-logging/>

虽然表面上看起来似乎有悖常理，但在许多情况下，将大量能量注入电阻，仅仅是为了将其转化为热量，对于电路的运行是必要的。这些情况大多涉及测试电源或无线电发射机等电子设备，虽然在某些情况下可以使用简单的电阻组，[这种有源假负载由不同的内部元件组成，具有一些额外的启动功能](https://sites.google.com/site/hobbydebraj/dummy-electrical-load-v2-0)。

由[Debraj]构建的负载库实际上是一个电子负载，这使它比电阻库等简单的无源假负载有更广泛的用途。它是专门为 DC 设计的，还包括电压测量、电流控制、温度测量和散热器风扇的速度控制。它还包括一个蓝牙模块，允许它通过自定义协议和 GUI 使用 python 与计算机通信。

虽然这款产品确实使用了另一款产品的外壳和一些其他器件，并且是专门为使用它们而设计的，但 PCB 原理图和代码都可以用于构建您自己的设计或扩展这种设计。它旨在用于 DC 应用，但也有其他虚拟负载可用于无线电天线设计等方面，[事实证明，您也可以从它们身上学到很多东西](https://hackaday.com/2015/12/24/you-can-learn-a-lot-from-a-dummy-load/)。

 [https://www.youtube.com/embed/-At_PHyIsFw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-At_PHyIsFw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

