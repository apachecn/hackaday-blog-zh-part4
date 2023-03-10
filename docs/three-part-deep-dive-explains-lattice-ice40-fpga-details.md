# 三部分深入讲解 Lattice ICE40 FPGA 细节

> 原文：<https://hackaday.com/2018/09/27/three-part-deep-dive-explains-lattice-ice40-fpga-details/>

我们喜欢 Lattice iCE40 FPGA 已经不是什么秘密了。它拥有廉价的开发板和开源工具链，因此是开始开发低成本、低功耗 FPGA 设计的简单方法。该系列中有几个成员具有相似的特征，包括顶级的 UltraPlus。Lattice 的[Steve]和加州大学欧文分校的[Michael Klopfer]制作了一个由三部分组成的视频系列，解释了这些设备的架构。总的来说，这些视频大约有一个小时长，当然，它们使用的是官方工具，而不是 IceStorm。但是，如果你有一个 iCE40 板，并且你想了解在引擎盖下的芯片有什么，它仍然是一个伟大的时间投资。

第一部分相当短，讲了很多应用。FPGAs 的业余使用也得到了认可。请记住，iCE40 FPGAs 有不同的尺寸和型号，所以当你看到他们提到 RISC-V 时不要激动——据我们所知，这不适合你的 iCEStick。冰棍上有一个 HX-1K，这是一个具有 1280 个逻辑元件的高性能版本，与低功耗(LP)版本相反。

事实上，您可能想打开数据手册观看视频。最低端的 UltraPlus 设备具有更多的逻辑元件(2，800 对 1，280)和更多的 RAM (1，104 千位对 64 千位)。它还具有专门的 I2C、SPI、DSP 和 PWM 板载硬件。虽然 HX-1K 缺乏这些额外的功能，但与低端 UltraPlus 的 21 I/O 相比，它最大允许 98 I/o。它们的最大传播延迟也更低，这意味着你通常可以让它们比该系列的其他成员更快。

然而，核心结构是相同的:一个四输入查找表(LUT4)、一个 D 触发器和一些进位逻辑。更现代的 FPGA 通常会有更多输入到 lut，以提供更密集的封装，因此在比较一个 FPGA 系列的单元数时要小心。

当然，如果你正在使用冰棍，你可能想升级到更强大的家庭成员，然后视频中的一切都将适用。他们使用升级版，这是一个很好的升级，而且仍然很便宜。第三个视频介绍了晶格专用工具。请注意，如果您想使用 Ultra 或 UltraPlus 设备，Icestorm 只支持其中的一部分。如果你使用 IceStorm，你会想了解一下[对新设备的支持](http://www.clifford.at/icestorm/ultraplus.html)。如果你还没有开始使用 FPGA，为什么不去 [Hackaday.io](https://hackaday.com/2018/08/06/learn-fpga-fast-with-hackadays-fpga-boot-camp/) 了解更多关于在 FPGA 训练营中使用 iCE40 的信息呢？

 [https://www.youtube.com/embed/DwxBkYhor80?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/DwxBkYhor80?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/UlgJ7TRU1KI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/UlgJ7TRU1KI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/6UgVUExXlvg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/6UgVUExXlvg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

