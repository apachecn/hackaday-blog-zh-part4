# 老思科广域网卡变成了 FPGA 游乐场

> 原文：<https://hackaday.com/2019/11/20/old-cisco-wan-card-turned-fpga-playground/>

我们许多人认为 FPGAs 是一些新的尖端技术，但事实是它们已经存在了相当长的一段时间。它们只是传统上被用在对我们这些低级黑客来说过于昂贵的硬件中。一个典型的例子是思科 HWIC-3G-CDMA 广域网卡。十年前，这些可能是价值数万美元的路由器的一部分，但今天在易贝，它们的价格不到 10 美元。在这个价格上，[Tom Verbeure]认为有必要弄清楚[它们是否可以被重新用作通用 FPGA 实验设备](https://tomverbeure.github.io/2019/11/11/Cisco-HWIC-3G-CDMA.html)。

为了不吊你胃口，简短的回答是响亮的是。最后，[汤姆]要做的就是弄清楚 HWIC-3G-CDMA 在 edge 连接器上的预期电压，并将一个 2×5 连接器焊接到有帮助标签的 JTAG 接头上。一旦通电并连接到计算机，英特尔的 Quartus 程序员软件立即拿起主板的 Cyclone II EP2C35F484C8 芯片。广告之后，视频中闪烁的发光二极管证明这些廉价的小玩意已经成熟，可以被黑客攻击了。

不幸的是，有一个陷阱。在研究了电路板上的其他组件后，[Tom]最终得出结论，HWIC-3G-CDMA 无法真正存储 FPGA 的比特流。想必是路由器自己在启动时提供的。如果你只是想把电路板拴在电脑上做实验，那也没什么大不了的。但如果你想在某种项目中使用它，你需要包括一个微控制器，能够将大约 1 MB 的比特流推入 FPGA。

它可能不像 [2019 Hackaday 超级大会徽章](https://hackaday.com/2019/11/04/gigantic-fpga-in-a-game-boy-form-factor-2019-supercon-badge-is-a-hardware-siren-song/)那样容易启动和运行，但它肯定更容易拿到手。

[https://player.vimeo.com/video/372548312](https://player.vimeo.com/video/372548312)