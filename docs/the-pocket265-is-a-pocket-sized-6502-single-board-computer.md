# Pocket265 是一台袖珍 6502 单板计算机

> 原文：<https://hackaday.com/2022/09/07/the-pocket265-is-a-pocket-sized-6502-single-board-computer/>

自从微处理器在 20 世纪 70 年代变得可承受以来，单板计算机就一直存在，从未消失过。今天，我们有 Raspberry Pis 和 LattePandas，而在 70 年代和 80 年代，有 Ferguson Big Board、KIM-1 和一系列英特尔 SDK 主板。虽然在功能上与现代主板相似，有 CPU、RAM、ROM 和一些基本的外围设备，但与今天的微型平台相比，旧主板非常庞大，通常需要相当强大的电源才能运行。

然而事情并不一定是这样，正如[Aleksander]用[展示的 Pocket265:一台有点让人想起著名的 KIM-1](https://github.com/agkaminski/Pocket265) 的手持 6502 单板计算机。像那台经典的机器一样，它有一个十六进制的键盘来输入使用机器代码的程序，还有一排 LED 显示屏来显示程序的输出。与 KIM 不同，Pocket265 小到足以单手握持，并使用气泡 LED 显示屏，这使它看起来更像 20 世纪 70 年代的可编程计算器。它配有锂电池，使其真正便携，还有一个光滑的 3D 打印外壳，比裸露的电路板更舒适。

单个 ROM 芯片包含一个运行基本用户界面的监控程序。它还通过实现大量系统调用来处理用户输入和显示输出之类的事情，使编程变得不那么乏味。串行 EEPROM 支持本地数据存储，而带有 USB 接口的 UART 支持向其它计算机传输数据。如果您对自己构建和编程这样的机器感兴趣，[Aleksander]在他的 GitHub 页面上提供了代码示例和完整的硬件文档。

6502 仍然是硬件黑客的最爱:我们最近推出的一些项目包括[一台制作精美的机器](https://hackaday.com/2022/07/29/perseus-9-the-dual-6502-portable-machine-that-should-have-been/)、[这种易于制造的单板计算机](https://hackaday.com/2021/02/12/everything-old-is-new-again-another-6502-board-is-born/)和[这种基于试验板的巨大装置](https://hackaday.com/2019/04/04/a-6502-computer-with-acres-of-breadboard-and-dozens-of-chips/)。在找小一点的吗？试试[这个整洁的小板子](https://hackaday.com/2017/02/20/a-6502-retrocomputer-in-a-very-tidy-package/)或者[这个耦合到 FPGA](https://hackaday.com/2020/11/03/brain-in-a-vat-6502/) 的 6502。