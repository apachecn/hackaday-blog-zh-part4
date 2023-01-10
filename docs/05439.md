# COSMAC ELF 重生了，在 FPGA 中

> 原文：<https://hackaday.com/2020/01/23/cosmac-elf-lives-again-in-fpga/>

环顾当今的个人计算市场，市场上似乎有很多选择。然而在现实中，几乎所有的东西都运行在一小群公司的硬件上，软件通常可以跨平台获得。在 20 世纪 70 年代和 80 年代的个人电脑热潮中，情况并非如此，不同的电脑在硬件甚至架构上都大相径庭。Cosmac ELF 是这个时代最有趣的标本之一，[它在 FPGA](https://hackaday.io/project/169486-fpga-cosmac-elf) 上被精心复制。

最初的硬件是基于 RCA 1802 微处理器，有一套基本的(以今天的标准)开关和按钮作为计算机的输入。即使在当时，它的成本也很低，但却是最早上市的单板计算机之一。这种娱乐是用 SpinalHDL 编码的，原始硬件的简单性使它相对容易理解。FPGA 对于原始硬件也是周期精确的，这使得它即使没有任何原始硬件也近乎完美。

该项目的创建者，[Winston]又名[wel97459]，发现 SpinalHDL 使这个项目变得有趣(并在他的 [GitHub 页面](https://github.com/wel97459/FPGACosmacELF)上发布了他的代码)，并能够将代码压缩到仅 1500 行来重建原始硬件。这给人留下了深刻的印象，对于任何对 70 年代早期计算机复兴时期[提供的一些更独特的计算机感兴趣的人来说，这也是一本容易阅读的书。](https://hackaday.com/2017/03/06/vintage-cosmac-elf-is-pretty-close-to-original/)