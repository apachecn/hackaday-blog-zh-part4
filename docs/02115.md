# 构建 RISC-V 桌面

> 原文：<https://hackaday.com/2019/02/11/building-a-risc-v-desktop/>

如果你想谈论 RISC-V，CPU 的开源指令集，你可能会谈论微控制器。你现在可以买到体积小但功能强大的 RISC-V 微处理器，价格相当于 ARM Cortex-M4 处理器。在管道深处是类似 SOC 的核心，你会在桌面 NAS 解决方案中找到这种核心，可能是一些路由器和智能电视。这很好，但我们对“电脑”的概念仍然是台式机。开放指令集桌面何时到来？嗯，它现在就在这里。【安德鲁回来】[造了一台 RISC-V 台式电脑](https://abopen.com/news/building-a-risc-v-pc/)。它运行 Linux，装在一个盒子里，有 HDMI 和 USB，还有一个显卡，可以工作。这是一台运行 RISC-V 内核的台式机。

这个版本的核心[是 HiFive Unleashed](https://hackaday.com/2018/02/03/sifive-introduces-risc-v-linux-capable-multicore-processor/) ，这是 SiFive 的一个支持 Linux 的主板，si five 是第一个(生产)RISC-V 微控制器的制造商。该主板使用采用 28 纳米工艺制造的 Freedom U540 SOC，具有 8GB DDR 4 和 32MB 闪存。对于一个建立在开放架构未来的主板来说，这令人印象深刻，但这是有代价的:HiFive Unleashed [在其众筹活动](https://www.crowdsupply.com/sifive/hifive-unleashed)中的价格高达 1000 美元。

但是带有开放式 CPU 的主板不是台式机。你需要外围 IO，也许几个 PCIe，希望还有 SATA 接口。这个问题已经被 Microsemi [用一个扩展板](https://www.crowdsupply.com/microsemi/hifive-unleashed-expansion-board)给 HiFive Unleashed 解决了。它包括一个大的现场可编程门阵列和所有你可以使用的连接器。也要 2000 美元。

随着大部分部件准备就绪，几个按钮，M.2 PCIe 和 SATA 固态硬盘存储，一个显卡和一个漂亮的丙烯酸外壳被添加进来。感谢 Western Digital，[构建 Linux 就像构建 Linux](https://github.com/westerndigitalcorporation/RISC-V-Linux/) 一样简单，最终你会得到一台带有 RISC-V 大脑的台式电脑。

与普通的“游戏机”相比，这是一款昂贵的产品。快速和肮脏的价格大约是 4000 美元左右的机器，可以让你检查你的脸书。有一个机器运行的视频，你可以在下面查看。

[https://player.vimeo.com/video/315869857](https://player.vimeo.com/video/315869857)