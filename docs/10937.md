# 老式测试设备上瘾是合理的

> 原文：<https://hackaday.com/2021/08/05/vintage-test-equipment-addiction-justified/>

Recore 3D 打印机板开发人员[Elias Bakken]发布了他使用四个(至少)老式惠普测试设备开发的自动测试程序。此外，他的测试夹具和测试理念也相当有趣。

除了做一个钉床测试夹具，他还设计了一个继电器多路复用板，从 23 个不同的电压中选择一个进行测量。我们喜欢他在该应用中选择的机械闭锁继电器，它不仅省电，而且不会使测试板受到任何磁场的影响(除非在切换状态时)。

在[Elias]的设置中，被测单元(UUT)实际上编排了测试过程本身。这并不像听起来那么疯狂。处理器高度集成在一个封装和外部 DRAM 中。如果 CPU 启动，并通过简单的自检程序，没有理由不利用板载处理器作为主要的测试控制计算机。如果您的处理器非常小，资源和连接性有限，这可能是一个有问题的决定。但在 Recore 的情况下，处理器是运行 Debian Linux 的四核 ARM A53 SoC 这种安排本身可以在其他项目中用作自动测试计算机。

在下面的视频中，[Elias]带领我们完成了基本测试，然后重点介绍 Recore 板测试的核心:校准输入信号调理电路。[Elias]没有使用非常昂贵的精密电阻，而是选择了更经济的 1%电阻用于前置放大器电路。这里的权衡是需要校准每个通道，也许是在多个温度点。在这种情况下，使用测试夹具、自动化测试脚本和一堆可编程测试设备会大放异彩。

[Elias]仍然在思考他在校准热电偶时发现的一些问题，所以他的冒险还没有完全结束。如果你想知道 Recore 是什么，可以看看六月份的这篇文章。你是否曾经使用电路板上的微处理器进行自我测试，无论是单独使用还是与外部夹具配合使用？请在下面的评论中告诉我们。

 [https://www.youtube.com/embed/2lFS3n8FOJk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/2lFS3n8FOJk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

