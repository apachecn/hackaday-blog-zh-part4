# 廉价 FPGA 中的 SPARC CPU

> 原文：<https://hackaday.com/2019/11/01/sparc-cpu-in-a-cheap-fpga/>

曾几何时，SPARC CPU 是昂贵的 Sun 工作站的唯一领域，但现在你可以轻松地在 FPGA 上安装一个。问题是你需要一个相当大的 FPGA，它并不总是便宜的，除非有人破产了，而你很幸运。[Ttsiodras]拿起一个 Pano 逻辑瘦客户端。Pano 破产了，他们所有的存货都在剩余市场上以低价出售。用一点 FPGA 的魔力，你可以把几块钱变成一台基于 SPARC 的计算机。

工作站的内部有一个 Spartan 6 FPGA，你需要焊接一些 JTAG 线，但这不应该让这里的任何人失望。当然，Spartan 6 不是最新的技术，所以你必须得到一个旧版本的 Xilinx 工具，但这也不难。然而，如果你使用 Linux，你需要注意一个奇怪的讽刺。

Xilinx 免费提供他们的 WebPack 工具，你可以下载旧版本。然而，版本并不总是相同的。在 Linux 上支持 Spartan 6 的最新工具不支持 Pano G2 中使用的特定设备。但是，Windows 版本可以。奇怪的是，Windows 版本安装了一个 Linux 虚拟环境来运行这些工具！

然而，故事并没有就此结束。[Ttsiodras]希望直接在 Linux 上运行这些工具，并尝试让它们全部运行起来。是的，但这是一个有趣的侦探故事，你可以在邮报上读到。如果你想使用 Windows 来配置 FPGA，你可能不会太在意，但这仍然是一个有趣的阅读。我们发现特别有趣的是，免费的 WebPack 软件仍然被节点锁定到特定的网卡上——我们在使用其他供应商的 FPGA 工具时也遇到过类似的问题。

莱昂是一个 SPARC CPU 用在许多欧洲航天器。这就是最终为[Ttsiodras]驱动 Pano 的 CPU。FPGA 足够大，他能够在机箱中获得两个 50 MHz 内核。你甚至可以在将 CPU 植入芯片之前对其进行模拟。

不幸的是，该版本不支持网络、板上的 128 MB 内存或 USB 端口。所以您还没有准备好将它用作您的日常 Linux 工作站。然而，有一个远程 gdb 接口和一个交叉编译器，所以你当然可以为它写代码。如果你不想焊接，[这个技术](https://hackaday.com/2019/04/19/pano-logic-fgpa-hacking-just-got-easier/)可能会有帮助。

使用现成的 CPU 可能是一个项目的重要启动。莱昂、 [RISC-V](https://hackaday.com/2019/02/13/western-digital-releases-their-risc-v-cores-to-the-world/) ，甚至 [NIOS](https://hackaday.com/2018/10/05/easy-fpga-cpu-with-max1000/) 给你现成的工具，这是一件好事，只要你的项目不是定制的 CPU。