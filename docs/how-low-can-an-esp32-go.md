# ESP32 能开到多低？

> 原文：<https://hackaday.com/2020/01/07/how-low-can-an-esp32-go/>

我们中的许多人都尝试过 ESP32 微控制器，被它的 WiFi 和强大的处理器内核所吸引，但有多少人会探索它的所有板载功能呢？这款芯片更有趣的功能之一是其超低功耗(ULP)协处理器，这是一个额外的核心，允许 ESP32 在关闭日益饥渴的主核心的情况下运行，同时消耗微量的功率。

这是一个功能，[Max Kern]在他的[低功耗 ESP32 手持电脑](https://hackaday.io/project/169103-low-power-esp32-handheld)中发挥了巨大作用，他将芯片与低功耗[夏普内存 LCD](https://www.sharpsma.com/products?sharpCategory=Memory%20LCD&p_p_parallel=0) 配对，并使用 ESP32 的 ULP 核心在 ESP 核心休眠时保持显示器活跃。软件方面，该设备支持基本的 PDA 和时钟功能，包括一个 RSS 解析器，所有这些都可以在休息时的视频中看到。它的灵感来自 Panic 配备曲柄的 Playdate 控制台，它与该控制台共享清晰的显示。

看到这个设备让我们想起了过去几年中我们看到的一些带有 ESP32 电源的徽章。一个活动徽章的创造者一直在努力让设备有足够的电池寿命来持续一段时间。这是一个问题，SHA 2017 徽章的设计师用电子墨水单元解决了这个问题，但也许夏普显示器可以为新设计提供一个具有成本效益的替代方案。

 [https://www.youtube.com/embed/IB07gSAHnkQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/IB07gSAHnkQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

