# 这是 Linux——但在 ESP32 上

> 原文：<https://hackaday.com/2021/07/21/its-linux-but-on-an-esp32/>

GNU/Linux 是一个开源奇迹，在过去的三十年里，它给了我们一个几乎无限通用和强大的类 UNIX 操作系统。但是，即使它也有其局限性，特别是在硬件规模的低端，功能不太完善的处理器通常缺乏内存管理单元等先决条件。因此[JuiceRV]在 ESP32 微控制器上启动 Linux 内核的壮举似乎是不可能的，发生了什么？

ESP 的双 32 位 Xtensa 内核在处理能力方面毫不逊色，但如果没有 MMU，它就不是一个明显的 Linux 候选平台。这个问题的解决方案以[的形式出现，一个仿真的 RISC-V 虚拟机](https://github.com/juiceRv/JuiceVm)，它为 Linux 5.0.0 内核引导提供了足够的咕噜声[。](https://www.reddit.com/r/esp32/comments/om106r/boot_linux_500_on_esp32/)

无论从哪方面来看，这都是一项令人印象深刻的工作，但是这种新发现的在微控制器上运行 Linux 的能力会席卷全球吗？当然不会，除非你的口味是最慢的计算体验。然而，这是黑客的本质，为此我们向它致敬。

这并不是 Linux 第一次在微控制器上运行，过去有人将 30 针 SIMM 和 SD 卡连接到 8 位 Atmel 芯片上，并以类似的方式用 ARM 仿真器进行操作。

通过 [CNX 软件](https://www.cnx-software.com/2021/07/18/linux-5-0-esp32-processor/)。

标题图像:Ubahnverleih， [CC0](https://commons.wikimedia.org/wiki/File:ESP32_on_Lolin32_Lite_clone_board.jpg) 。