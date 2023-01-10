# HVTPI 初级读本和工具包为您提供 BOM 替代工具

> 原文：<https://hackaday.com/2022/02/28/hvtpi-primer-and-toolkit-equips-you-for-bom-substitutions/>

新颖的 MCU 编程接口可能会让我们大吃一惊，但随后我们不可避免地会跟上所需的变化。[今天的堡垒是 hvt pi](https://hackaday.io/project/184003)——我们刚刚开始习惯的 TPI 的“12V 复位”附加物，并且[Sam Ettinger]分享了一个简单的电路来教我们所有关于它的知识，以及 PCB 文件和它如何工作的详细解释。

HVTPI 是 TPI 之上的一个附加组件，正如 Sam 解释的那样，当 TPI 希望它为低逻辑电平时，你需要将 RST 保持在 12V，否则保持在 Vtarget。为此，他设计了各种不同复杂程度和要求的转接板；[解释每一个选择背后的含义](https://hackaday.io/project/184003/details)并消除可能出现的误解。所有的董事会文件(和 TPI 写的副本)[也在 git 仓库中与我们分享](https://github.com/settinger/HV_TPI_tool)！因此，[如果你有一个 USB-ASP](https://hackaday.com/2021/05/03/teaching-a-usbasp-programmer-to-speak-tpi/) 或[Arduino](https://hackaday.com/2012/08/23/programming-the-attiny10-with-an-arduino/)可用，现在你也有一切可以做 HVTPI，感谢 Sam 的工作和解释。

在之前，我们已经[报道了山姆的事迹，不禁对沿途停下来解释的弯路心存感激。HVTPI 被用在非常小的零件上，我们想知道](https://hackaday.com/2021/10/16/unique-seven-segment-display-relies-on-fr-4-fluorescence/)[最近的 FPC 板中是否有新的东西能够完全安装在 C 型电缆端](https://hackaday.com/2022/01/01/genius-or-cursed-this-usb-c-connector-is-flexible/)中并发挥作用！

随着芯片短缺，研究小型和模糊的库存微控制器的编程接口已经得到了回报，如果你有一些需要微控制器但不会消耗大量资源的项目，可能是时候[尝试一下 ATTiny10 了](https://hackaday.com/2016/03/01/breaking-out-the-attiny10/)。最坏会发生什么——你让[成为有史以来最小的芯片音乐](https://hackaday.com/2012/08/14/making-chiptunes-with-32-bytes-of-ram/)？