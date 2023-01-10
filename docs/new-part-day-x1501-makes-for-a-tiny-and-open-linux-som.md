# 新的部分日:X1501 有助于一个小而开放的 Linux SoM

> 原文：<https://hackaday.com/2022/06/05/new-part-day-x1501-makes-for-a-tiny-and-open-linux-som/>

曾经想在极小的内存中运行 Linux 吗？然后【SudoMaker】的【Reimu NotMoe】有东西给你！她在 BGA 中发现了一个难以置信的小 Linux 芯片，并设计了一个自带电源管理和城堡状焊盘的小型 SoM(模块上系统)突破。这个突破包含了在 16x16x2mm 的空间中运行 Linux 所需的一切。作为参考，一个 16 毫米的正方形相当于树莓派上 CPU 的大小。

该板不仅小巧，而且经过精心设计，帮助您以最小的努力将 BGA 封装的 Ingenic X1501 放在任何地方。有了齿形焊盘，就可以很容易地手工焊接这种 SoM 进行开发和回流生产。板载开关调节器的工作电压范围为 6V 至 3V，因此这是一个可行的电池供电 Linux 选项。它甚至可以为您的所有外部设备提供高达 3.3V/1A 的电压。

迄今为止最酷的部分 X1501 出奇的友好，没有 NDA。[数据表可供索取，](https://hackaday.io/project/185562-x1501-pico-som#menu-files)没有“机密”水印——你得到的是一份 730 页的 PDF 文件。由于这种开放性，X1501 可以运行主线 Linux，只需进行最小的更改，并且已经支持大多数外围设备。此外，如果您的软件需要防止克隆，还有基于 Efuse 的安全引导。

休息后更多…

X1501 有什么好酷的？Ingenic X1501 是一个内置 RAM 的可爱小 BGA，没有高速路由问题。当然，你只能得到 8M 的内存，但是你可以把 Linux 拆成一大堆—[一半的内存是免费的](https://hackaday.io/project/185562/gallery#e038300bffd3d94a4547a5786a6b4c2f)供你自己使用。你可以在 Linux 上用少量的内存做很多事情，就像我们今年看到的 15 美元的 Linux 电脑一样。

我们已经看到基因制造的芯片将 Linux 带到了一系列廉价产品中，从[游戏机](https://boards.dingoonity.org/ingenic-jz4760-devices/ingenic-devices-guide/)到[小型黑客安全摄像头。](https://hackaday.com/2018/03/05/customising-a-30-ip-camera-for-fun/)如果你厌倦了让你头疼的 MCU，也许你想从 Linux 提供的所有接口、库、语言和框架中受益。这个 SoM 是简化开发的一个极好的垫脚石。

你得到一个 1GHz 的 MIPS32r2 内核，一个备用的 300MHz 内核用于所有的实时任务；2MB 的内部闪存适合 Uboot 和一个有足够空间的 Linux 内核。你可以连接一个 MicroSD 卡来存储更多信息。您还可以获得所有接口，如 USB、SPI、I2C 和 SDIO，以及模拟和数字音频支持。有一点 DMA 的小问题，但是没有什么不能通过一点时间和社区的帮助来解决的。

说到一个社区——[灵梦]说她已经为众筹推出了这个板，所以请留意。如果有人有兴趣帮助改进内核的怪癖，一些面向开发人员的单元肯定会出现在桌面上！众筹完成后，所有的设计文件都将是开源的——否则，这样的电路板对其他人来说将是微不足道的。如果你想要这样一个模块的一些很酷的项目想法——一个小小的 Linux 驱动的手机怎么样？这个里面有一个 Ingenic X1000。

你想知道这样的板子是怎么做出来的吗？我们已经看到了一篇令人印象深刻的关于用定制的 PCB 和 Linux 驯服小型 ARM 芯片的文章！

> 使 USB 主机模式在 [#X1501](https://twitter.com/hashtag/X1501?src=hash&ref_src=twsrc%5Etfw) Pico 上工作。Linux 内核 v5.19 即将发布补丁。【pic.twitter.com/QILjcZ4PfV T3
> 
> —ReimuNotMoe(@ ReimuNotMoe)[2022 年 5 月 30 日](https://twitter.com/ReimuNotMoe/status/1531321048892788737?ref_src=twsrc%5Etfw)