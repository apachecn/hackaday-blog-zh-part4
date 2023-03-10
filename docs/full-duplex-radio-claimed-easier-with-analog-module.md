# 全双工无线电声称使用模拟模块更容易

> 原文：<https://hackaday.com/2020/01/06/full-duplex-radio-claimed-easier-with-analog-module/>

有一句老话说，我们有一张嘴和两只耳朵，所以你可以听两倍于你说的。然而，边听边说是相当困难的，尤其是在无线电信号的情况下。一家名为 [Kumu Networks 的公司有一个模拟模块，可以使用自干扰消除](http://kumunetworks.com/)，允许在收发器中以大约 50 dB 的发射信号在同一频率上发射和接收。你可以在下面看到一个关于 Kumu 声称其技术的视频。

你可能会认为手机和业余无线电转发器同时发射和接收，这当然是事实，但通常是在不同的频率上，以避免直接干扰。双工器是一种将两种频率分离出来的设备，而双工器是根据信号的方向将它们分离出来，但它们很难使用。在雷达等应用中，双工器可以在单个频率上工作，即使这样，也很难防止发射机的泄漏导致接收机过载和灵敏度降低。

虽然 50 dB 听起来不算多，但它是 100，000 的倍数，这应该为无线电发射机和接收机甚至在同一频率上共存开辟了新的机会。该设备是模拟的，因此它使用电路来反转传输的信号，并在接收器处重新合并。

[IEEE Spectrum](https://spectrum.ieee.org/telecom/wireless/kumu-networks-launches-an-analog-radio-module-that-cancels-its-own-interference) 最近有一个帖子声称该公司正在发布 K6 模块，可以“轻松安装在几乎任何无线系统中”射频看起来像是黑魔法，但我们可以想象这在理论上应该如何工作。您需要调整反相网络的相位，以匹配拾取信号的位置(大概在功率放大之前)与接收机混合抵消信号的位置之间的相位延迟。

听起来不错，但话说回来，降噪耳机听起来也很简单，我们都知道，即使是一副昂贵的耳机也有不尽人意的地方。

 [https://www.youtube.com/embed/9wyYWKIagM4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/9wyYWKIagM4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

