# 3D 打印机失控测试

> 原文：<https://hackaday.com/2021/09/01/test-for-3d-printer-runaway/>

一些 3D 打印机因爆发而获得了应有的声誉。如今，大多数(但显然不是所有)打印机都有固件，可以检测可能导致火灾的常见问题。如果你编写自己的固件，你可以检查你是否有保护，但如果你有一台来历不明的打印机呢？[Thomas]向您展示如何[检查安全打印机](https://toms3d.org/2021/08/20/test-your-printers-for-thermal-runaway/)。也看看他的视频，嵌入下面。

这个想法是假装会引起问题的那种失败。首先，当热敏电阻读数不正确时，您需要打开加热器。如果热敏电阻的读数一直很低或者是环境温度，那么就有可能驱动加热元件变得越来越热。这不会总是导致火灾，但它可能会导致有毒气体。

当然，如果热敏电阻读数过高，应该会自行解决，因为固件应该只是关闭加热器，等待温度下降，但它不会这样做。我们之前有一个热敏电阻弹出，我们也有一个微小的热敏电阻断线，并进行间歇性连接。正确的固件会检测到这一点并停止加热。[Thomas]通过故意移除加热器或热敏电阻以及拔掉热敏电阻来模拟这种情况。

他试了两台打印机，一台 Ender 3，一台 Aquila。安德 3 是安全的，尽管令人惊讶的是它在出错时重启了。另一方面，这肯定会关掉加热器，所以这很好。然而，Aquila 令人失望，因为它在一些故障模式下冻结并保持加热。

当然，还有其他可能导致问题的事情，所以仅仅通过这些测试并不是完全安全的免费通行证，但它是一个很好的指标。例如，FET 短路(或 PCB 短路)可能导致加热器开启，而固件无法关闭加热器。不过，这应该很少见。这些其他模式更有可能。

我们对变热的工具并不陌生。烙铁、热风枪，甚至我们的厨房用具都在这样做。但是 3D 打印机似乎有更多的潜在问题，有关于它们被烧毁的惊人故事。[坏的连接器](https://hackaday.com/2016/12/07/dont-leave-3d-printers-unattended-they-can-catch-fire/)通常是罪魁祸首，但即使你确定你的连接器、电源和固件，你也不应该让打印机无人看管。

 [https://www.youtube.com/embed/eGUPBoDxmKk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/eGUPBoDxmKk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

