# 你将建造的最简单的 FT8 收发器

> 原文：<https://hackaday.com/2021/09/25/the-simplest-ft8-transceiver-youll-ever-build/>

或许 2021 年业余无线电最有趣的方面在于数字模式领域。使用软件无线电的无限可能性将数字无线电通信从仅使用模拟电子设备所能实现的限制中解放出来，因此这是一个无线电业余爱好者仍能领先于技术曲线的罕见领域。这些较新的数字模式之一是由多产的[乔泰勒 K1JT]创造的 FT8。

正是针对这种模式，[查尔斯·希尔] [创造了一种易于制造的收发器](https://github.com/chillmf/Pocket-FT8)。它的大脑是 aTeensy 3.6，而接收端是一个 [Si4735](https://www.skyworksinc.com/en/products/audio-and-radio/si4734-35-am-fm-sw-lw-radio-receivers/si4735) 接收芯片，发送端是一个 [Si5351](https://www.skyworksinc.com/-/media/Skyworks/SL/documents/public/data-sheets/Si5351-B.pdf) 可编程时钟芯片，驱动一个带有适当滤波器的 Mini-Circuits GVA84 功率放大器。界面通过触摸屏显示。它依赖于对 Si4735 接收机芯片即时应用补丁以接收 SSB 的现有工作，以及针对 FT8 软件的另一个项目。

这种收发器的魅力在于它几乎可以完全由模块组装而成。一些业余无线电爱好者可能会抱怨说，自制收音机应该只使用根据基本原理组装的最基本的组件，但显而易见的答案应该是，任何使收音机构造更容易的东西都是受欢迎的。如果 100 mW 的输出功率似乎有点低，那么值得记住的是，FT8 是一种弱信号模式，如果传播条件正确，尽管输出微弱，世界也应该能够听到它。

我们展示了不少使用 Si47XX 系列的收音机，[它们可以被制成非常整洁的接收器](https://hackaday.com/2020/02/12/all-band-radio-uses-arduino-and-si4730/)。