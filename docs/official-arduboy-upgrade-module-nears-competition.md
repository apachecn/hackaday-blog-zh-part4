# 官方 Arduboy 升级模块接近竞争

> 原文：<https://hackaday.com/2020/08/04/official-arduboy-upgrade-module-nears-competition/>

自从 2014 年[凯文·贝茨]展示了第一个原型以来，我们一直是 Arduboy 的忠实粉丝。这是一个制作和玩简单游戏的绝佳平台，但当然还有改进的空间。一个最明显的可用性问题一直是硬件一次只能容纳一个游戏。但是多亏了官方插件的开发，Arduboy 很快将有足够的存储空间来容纳数百款游戏

[![](img/eb8d5d253de6fd14d06f903683125601.png)](https://hackaday.com/wp-content/uploads/2020/08/arduboyfx_detail.jpg)

Even the rear silkscreen was a community effort.

升级采用小型柔性 PCB 的形式，焊接到 Arduboy 上现有的测试点。改装板配备了 W25Q128 闪存芯片，为手持设备的 ATmega32u4 微控制器提供了额外的 16 MB 闪存存储空间；足以容纳几乎所有为该平台编写的游戏和程序。

当然，将 SPI 闪存芯片连接到手持设备的 MCU 只是成功的一半。该系统还需要将其引导加载程序替换为能够感知这种扩展存储的引导加载程序。为此，升级板还包含一个 ATtiny85 来处理这个过程，而不需要外部程序员。虽然这对于普通的黑客读者来说是一种奢侈，但对于面向更广泛受众的升级来说，这是一个明智之举。

[升级板目前可供预购](https://arduboy.com/store/arduboy-fx-mod-chip/)，但是那些熟悉烙铁和 USBasp 的人现在可以通过跟随【Kevin】和“猎鹰计划”论坛中的社区之间的技术讨论[来升级他们自己的硬件。事实上，特别敏锐的读者可能会注意到，这次官方升级源于我们去年报道的](https://community.arduboy.com/c/development/project-falcon/46)[社区开发的 Arduboy 墨盒](https://hackaday.com/2019/06/07/the-arduboy-community-rolled-their-own-cartridge/)。

 [https://www.youtube.com/embed/xwe4bd6IsEg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/xwe4bd6IsEg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

