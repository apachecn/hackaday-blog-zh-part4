# STM32 是一款廉价的 DIY USB 声卡

> 原文：<https://hackaday.com/2022/05/24/the-stm32-makes-for-a-cheap-diy-usb-soundcard/>

声卡曾经是巨大的 8 位 ISA，会在台式计算机中占据大量的空间。如今，对于我们大多数人来说，它们已经被植入主板，我们几乎不再考虑它们。[萨姆索诺夫·马頔]决定开发一款他们自己的廉价小声卡，不过，[是围绕 STM32](https://hackaday.io/project/185213-stm32-hifi-usb-sound-card-diy) 开发的。

声卡特别基于 STM32F401。在“绿色药丸”开发板上随时可用。板上实现的数模转换器基于两个 PWM 定时器，可提供高质量输出。还有一个模拟软件 sigma delta ADC，在通过 USB 输入的音频流和实际的 PWM 输出之间实现，使用一些花哨的技巧来改善声音输出。[Samsonov]甚至找到时间添加了一个带有双 VU 计的显示器，显示通过左右声道泵送的音频。

手头没有测试设备，我们不能轻易量化声卡的性能。然而，根据 Youtube 上发布的视频来看，它似乎更有能力以良好的保真度和大量的细节再现音乐。

如果你需要一个便宜，简单的 USB 声卡，你可以用它来破解，这可能就是你要的。然而，如果你需要更适合老式电脑的东西，[考虑用这个代替](https://hackaday.com/2016/10/03/a-reproduction-vintage-sound-card/)。休息后的视频。

 [https://www.youtube.com/embed/KB1A08Pj6nc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/KB1A08Pj6nc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/TnEBuS5ONsY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/TnEBuS5ONsY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

