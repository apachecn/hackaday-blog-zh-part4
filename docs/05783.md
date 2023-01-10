# 在你的 Hackaday Superconference 徽章上观看 Linux 启动

> 原文：<https://hackaday.com/2020/02/29/watch-linux-boot-on-your-hackaday-superconference-badge/>

去年的 Hackaday Superconference 徽章是一个电子产品，将 ECP5 FPGA 打包成一个类似 Game Boy 的形状，并安装了 RISC-V 内核，这两者一起提供了几乎无限的徽章黑客潜力。然而，它没有运行 Linux，这是[Greg Davill]已经解决的问题，因为他不仅在他的徽章上运行 Linux，而且还有一个帧缓冲区[，允许他将徽章屏幕用作 Linux 终端屏幕](https://twitter.com/GregDavill/status/1231082623633543168)。最后，您可以在您的超级会议徽章上观看 Linux 引导，而不是通过它的串行端口。

他基本上通过改变一切实现了这一点:从新的 [VexRiscv](https://github.com/SpinalHDL/VexRiscv) CPU 内核，到新的视频驱动程序和[由 Frank Buss 提供的 VGA 终端](https://twitter.com/GregDavill/status/1231025277863526400)，现在[是 LiteVideo 项目的一部分](https://github.com/enjoy-digital/litevideo/tree/master/litevideo/terminal)。它还不是一个完全成熟的 Linux 平台，但是如果你想亲自尝试的话，你可以在 GitHub 库中找到它。翻一翻他的 Twitter feed ,可以看到他在过去几个月里为这项工作付出的努力，并表明这不是一项容易的任务。

对于那些在家记录分数的人来说，这是一个开放的硬件设计，运行开放的 CPU 核心，带有社区设计的开源外围设备，由开源工具链编译，运行开源操作系统。这只是徽章的精彩演示，展示了整个系统的灵活性。为 Hackaday 写作的最大好处之一是我们的社区能够创作出大量令人惊叹的作品，这就是这种能量的一个范例。我们迫不及待地想看看格雷格和其他任何试图尝试它的读者会想出什么。

如果你想重温一下 2019 年的 Supercon 徽章，[这里是我们在](https://hackaday.com/2019/11/04/gigantic-fpga-in-a-game-boy-form-factor-2019-supercon-badge-is-a-hardware-siren-song/)时的报道。