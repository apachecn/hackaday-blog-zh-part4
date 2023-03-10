# 通过 USB 供电为 LiPos 充电

> 原文：<https://hackaday.com/2019/02/23/charging-lipos-with-usb-power-delivery/>

DC 电源板从来都不是运行家用电器的好方法。它们又重又笨重，容易掉出来，堵塞邻近的插座。近年来，越来越多的设备都配有 USB 端口用于电源输入。然而，USB 供电总是充满了不同的公司使用各种不同的方法在充电器和硬件之间传递安全电流限制。

如今，我们很幸运地拥有了官方的 USB 供电标准。现在连笔记本电脑充电器都在用 USB 了，[【FPVtv 无人机】决定看看有没有可能用这样的设备作为大电流电源给电池充电](https://www.youtube.com/watch?v=f0bsQFx1ulo)。

测试从一个 MI 牌 USB C 笔记本充电器开始。插入 USB 功率计以确定充电器的电压和电流输出，同时使用小型微控制器设备与笔记本电脑充电器通信，并将其设置为高电压、高电流传输模式。然后插入锂电池充电器，通过以超过 1.4 安培的电流同时给两个大的 4 芯 LiPos 充电来测试设置。

该设置表明，使用正确的现成模块，只要你能欺骗它切换到正确的模式，就可以使用笔记本电脑充电器来运行高电流设备。这是 USB 电源技术的自然发展——这条道路始于很久以前[的 MintyBoost 等项目，早在](https://hackaday.com/2006/05/31/minty-boost-aa-based-usb-charger/)的时候。休息后的视频。

 [https://www.youtube.com/embed/f0bsQFx1ulo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/f0bsQFx1ulo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

