# 软件无线电获得物理控制

> 原文：<https://hackaday.com/2019/12/12/software-defined-radio-gets-physical-control/>

软件无线电(SDR)是一项伟大的技术，但旋转物理旋钮来浏览电波也是如此令人满意。为了恢复这种触觉体验，[Tysonpower]购买了一个便宜的 USB 音量旋钮，并着手让它与他的软件一起工作。不幸的是，[启动并运行它比你可能预期的要多得多。](https://tysonpower.de/blog/reprogramming-a-audio-knob-to-build-a-sdr-vfo-knob)

[![](img/59d8d75050c7a7fca64b5293fa90de8c.png)](https://hackaday.com/wp-content/uploads/2019/12/sdrknob_detail.jpg)

Programming the knob’s STM32

在验证了旋钮可以在他的计算机上进行音量控制后，[Tysonpower]决定尝试从设备的 STM32 微控制器中取出固件。不幸的是，这就是事情变得棘手的地方。原来芯片启用了代码保护，所以当它连接到程序员并进入 DFU 模式时，固件被清除了。哎呀。

这让[Tysonpower]别无选择，只能从头开始编写新的固件，这自然需要对设备的硬件进行逆向工程。第一步是阅读 STM32 开发并让工具链工作，这为旋钮的 LED 闪烁铺平了道路。几个多小时的工作和一些万用表戳后，他能够读取旋钮的运动。他描述说，由于缺乏文档，让 USB HID 工作就像一场噩梦，但最终他也解决了这个问题。

最终结果是固件允许音量旋钮模仿鼠标滚轮，这可以用于在许多 SDR 包中进行调谐。但我们认为真正的成功故事是[Tysonpower]通过逆向工程和 STM32 平台获得的经验。毕竟，有时候旅程和最终结果一样重要。

 [https://www.youtube.com/embed/_sxHZujkXbg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_sxHZujkXbg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

