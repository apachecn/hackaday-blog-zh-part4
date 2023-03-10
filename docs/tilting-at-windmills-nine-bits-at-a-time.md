# 一次倾斜风车九点

> 原文：<https://hackaday.com/2022/02/11/tilting-at-windmills-nine-bits-at-a-time/>

在过去——我们说的是 20 世纪 60 年代和 70 年代——计算机通常是为非常特殊的目的而制造的，使用离散逻辑或“位片”芯片。无论哪种方式，更多的位意味着更多的钱，所以这些计算机通常是用足够的位来满足所需的精度。然而，我们不认为当他决定在 FPGA 上实现一个名为 QIXOTE-1 的 [9 位 CPU 时,【Mad Ned】有这个想法。](https://madned.substack.com/p/holy-nonads-a-nine-bit-computer)

像许多业余爱好项目一样，这个项目从寻找问题的 FPGA 板开始。起初，[Ned]计划创建一台定制计算机和一种定制语言，然后制作一个视频游戏。在互联网上快速搜索一下，就会发现这是一个很常见的项目，我们在 Hackaday 上谈论过的一个人在[离开公园](https://hackaday.com/2017/01/13/fpga-computer-covers-a-to-z/)之前参与了这个项目。

[Ned]然后想做一个没有软件的视频游戏。第一个这么做太晚了。没有被吓倒，他决定复制 PDP-8。哎呦。以前也有人这么做过。想要一些原创的东西，他最终决定定制 CPU。因为字节通常是——如果不是技术上的——8 位，这个 CPU 称它的 9 位字为九进制，并使用八进制，每个九进制很好地映射到三位数。

第一篇文章讲述了 CPU 背后的故事，并简要概述了它的功能，但我们等待未来的文章来展示更多幕后的东西，也就是[Ned]所说的“神圣的 Nonads，第 010 部分”

定制 CPU 的缺点是你必须[建立自己的工具](https://hackaday.com/2015/07/31/build-your-own-cpu-thats-the-easy-part/)。当然，你总是可以[复制一些东西](https://hackaday.com/2019/11/01/sparc-cpu-in-a-cheap-fpga/)，然后偷走你的[工具链](https://hackaday.com/2019/11/19/emulating-risc-v-on-an-fpga/)。或者[通用](https://hackaday.com/2015/08/06/hacking-a-universal-assembler/)。