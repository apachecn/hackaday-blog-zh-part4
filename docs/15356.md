# 用 Raspberry Pi 和 FPGA 仿真任何 ISA 卡

> 原文：<https://hackaday.com/2022/11/13/emulate-any-isa-card-with-a-raspberry-pi-and-an-fpga/>

IBM PC 平台在 20 世纪 80 年代中期成为台式 PC 的主导标准的原因之一是它的开放式硬件设计，它基于后来被称为 ISA 总线的东西。任何制造商都可以设计出硬件和软件都与 IBM PC 兼容的插卡，甚至是整台计算机。尽管自 20 世纪 90 年代末以来，ISA 在大多数情况下已经过时，但一些 ISA 卡(如高质量声卡)在逆向计算爱好者中变得非常流行，现在在易贝上可以卖到数百美元。

那么如果你最喜欢的 ISA 卡不容易拿到怎么办呢？一种选择是前往[eigenco]的 GitHub 页面，查看他的 FrankenPiFPGA 项目。它包含一个简单的 ISA 插件卡的设计，可以连接到 Cyclone IV FPGA 和 Raspberry Pi。FPGA 连接到 ISA 总线并实现其总线架构，而 Pi 通过其 GPIO 端口与 FPGA 通信，并在软件中仿真您想要的任何卡。[eigenco]当前的存储库包含几个声卡以及一个硬盘和一个串行鼠标的代码。Pi 的多核架构允许它同时运行多个任务，同时保持 ISA 总线所需的合理的高数据速率。

在下面嵌入的视频中，您可以看到[eigenco]在 386 主板上演示该系统，该主板只有一个 VGA 卡来连接显示器。通过在 Pi 上模拟硬盘和声卡，他能够运行各种具有完整音效和音乐的经典 DOS 游戏。目前支持的声卡包括 AdLib、8 位 SoundBlaster、Gravis Ultrasound 和 Roland MT-32，但任何记录足够好的声卡都可以被模拟。

这种方法也可以方便地取代其他 unobtanium 硬件，如[罕见的 CD-ROM 接口](https://hackaday.com/2022/10/04/reverse-engineering-an-isa-card-to-revive-an-ancient-cd-rom-drive/)。当然，你可以将这个概念发挥到逻辑的极致，简单地用 FPGA 实现整个 PC[。](https://hackaday.com/2017/11/03/386-too-much-try-a-186-in-an-fpga/)

 [https://www.youtube.com/embed/1ej76w8sHxY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1ej76w8sHxY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/CkwgHHmKaSI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/CkwgHHmKaSI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

