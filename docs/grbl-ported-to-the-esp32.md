# Grbl 移植到 ESP32

> 原文：<https://hackaday.com/2018/07/26/grbl-ported-to-the-esp32/>

如果你正在建立一个数控或激光，有一个很好的机会，你将使用 Grbl 来移动。这也是一个相当安全的赌注，你最终会运行它的一些变化的 Arduino 坐在一个电机控制器分线板。它便宜，易于安装和使用，并且是 DIY 机器的有效“行业”标准，因此不缺乏信息。有什么不喜欢的？

[![](img/ecacd2059188b3a7d18fabc71cad239d.png)](https://hackaday.com/wp-content/uploads/2018/07/espgrbl_thumb.jpg) 嗯，事实上相当多的事情。正如[bdring]所解释的，Grbl 将 Arduino 的能力推向了极限；使其成为未来发展的死胡同。此外，Arduino 需要通过 USB 插入主机才能工作，这对 2018 年的许多人来说是一个相当古怪的想法。[这些只是他决定将 Grbl 移植到 ESP32 委员会](http://www.buildlog.net/blog/2018/07/grbl-cnc-firmware-on-esp32/)的部分原因。

就价格而言，Arduino 和 ESP32 差不多，但 ESP 确实比 8 位意大利种马更强大。它有更多的闪存和内存，也许最重要的是，包括 Wi-Fi 和蓝牙。它仍然需要插入电路板，以容纳 Arduino 等电机驱动器，但除此之外，[bdring]认为 ESP32 几乎是你能得到的最完美的 Grbl 平台。

[bdring]报道称，将代码移植到 ESP32 上并不可怕，但也不完全是在公园散步。大部分代码没有遇到太多麻烦，但是到了需要精确计时的部分，事情就变得棘手了。ESP32 使用实时操作系统(RTOS ),它不太乐意放弃对硬件的控制。关闭 RTOS 是一种选择，但这将摧毁蓝牙和 Wi-Fi，因此显然不是一个理想的解决方案。最终，他想出了如何让中断或多或少地与 RTOS 配合，但提到在他准备向公众发布固件之前，还有一些工作要做。

如果你浏览 Hackaday 有一段时间了，你可能还记得[bdring]。他对让东西动起来很有一套，最近他创造了一系列[神奇的小型数控机器，这些机器绝对吸引了我们的眼球。](https://hackaday.com/2017/12/28/coasty-the-coaster-toaster/)

【感谢乔恩和克雷格的提示。]

 [https://www.youtube.com/embed/A9TNu58Sq00?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/A9TNu58Sq00?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

