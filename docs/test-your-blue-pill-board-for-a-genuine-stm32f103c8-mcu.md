# 为真正的 STM32F103C8 MCU 测试您的“Blue Pill”板

> 原文：<https://hackaday.com/2021/06/23/test-your-blue-pill-board-for-a-genuine-stm32f103c8-mcu/>

随着基于 STM32F103C8 的“蓝色药丸”电路板市场慢慢被含有克隆、假冒或直接损坏芯片的电路板所淹没，[特里·波特]真的希望有一种简单、自动化的方法来快速检测新电路板是否含有真正的 STM32 硅，或者一些试图看起来像部件的假冒产品。经过一年多的工作，蓝色药丸诊断项目已经准备就绪。

我们[之前已经介绍过](https://hackaday.com/2020/10/22/stm32-clones-the-good-the-bad-and-the-ugly/)那些克隆 MCU。很明显，一些“蓝色药丸”电路板上显然没有真正的 STM32 MCU，因为它们没有 STM32 标记，而其他人则在包装上伪造这些标记，很难识别。通常只有测试 MCU 的实际功能才能明确它是否是真正的 STM32 MCU。

这些诊断不仅允许测试 64 kB 的闪存，还允许测试这些 MCU 上常见的 64 kB 的“隐藏”闪存(重新标记的 128 kB STM32F103 内核)。它进一步检查制造商 JDEC 代码，并在真正的 STM32F1xx MCUs 中使用硅缺陷，其中 BGMCU_IDCODE 在没有连接 SWD 或 JTAG 的情况下无法读取。

Blue Pill Diagnostics 的另一个有趣的特性是使用 Mecrisp-Stellaris Forth 作为其基础，这也允许通过该固件轻松访问 Forth shell，这与 MicroPython 和 Lua 不同，只是这些固件所需闪存的一小部分。我们之前写过关于在你的项目中使用 Mecrisp-Stellaris 的文章。