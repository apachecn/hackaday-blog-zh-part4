# 一种通过电压故障使 Starlink 用户终端扎根的 Modchip

> 原文：<https://hackaday.com/2022/11/28/a-modchip-to-root-starlink-user-terminal-through-voltage-glitching/>

modchip 是一个小 PCB，直接安装在一个更大的电路板上，接入电路板上的点，让它做一些它不打算做的事情。我们通常会看到过去的游戏控制台使用 modchips，以一种软件黑客无法做到的方式绕过 DRM 保护。随着软件复杂性的增加，新游戏机上的攻击面也随之增加，软件黑客已经登上舞台。然而，在更加集成的硬件上，我们仍然希望回到老方法——这就是 Starlink 终端基于 modchip 的黑客带给我们的东西。

[伦纳特·伍特斯]“团队一直在戳戳 Starlink 用户终端，试图获得 root 访问权限，需要绕过 ARM 可信固件启动时完整性检查。该终端的 PCB 是碟形卫星天线大小，所以像激光故障注入这样的事情很难设置-因此，他们走了电压注入路线。后来，他们开发了一种可靠的方法，让 CPU 误操作来验证有问题的固件，并找到了根外壳——下面嵌入的 BlackHat talk 描述了这个旅程[。](https://www.youtube.com/watch?v=NXqLMmGwJm0)

为了使黑客更紧凑，可重复和便宜，他们决定将它从一堆电线和电路板转移到超薄外形，这就是 modchip 设计的由来。为此，他们将终端 PCB 放入扫描仪中，描绘出电路板轮廓，将其加载到 KiCad 中，并将所有必要的电压毛刺和监控部件放在一块电路板上，由久负盛名的 RP2040 驱动——如果您想在 Starlink 用户终端上扎根，该电路板拥有您需要的一切。由于 modchip 设计的灵活性，当 Starlink 发布固件更新，禁用用于监控的 UART 输出时，他们可以轻松地将信号重新路由到 eMMC 数据线。目前，KiCad 源文件不可用，但 GitHub 上有 Gerber 和 BOM 文件[，以防我们想要自己制作！](https://github.com/KULeuven-COSIC/Starlink-FI/tree/main/pcb)

毫无疑问，像这样的黑客为我们绕过安全保护所能达到的目标设立了一个新的标杆。黑客们一直在设计各种各样的 modchips，既有专有的也有开放的技术——我们已经看到一种可以让你在你的“智能”空气净化器中使用第三方过滤器，另一种可以让你在某些 3D 打印机上使用自己的灯丝，但还有一种可以让你在 ArduBoy 上添加大量游戏。特别是 RP2040，就在今年，我们已经看到了用于构建[任天堂 64 flash cart、](https://hackaday.com/2022/06/24/what-do-you-get-when-a-raspberry-pi-pico-flashes-a-nintendo-64/)PlayStation 1 存储卡、和[将自制支持添加到 GameCube 的 mod。](https://hackaday.com/2022/07/05/raspberry-pi-pico-modchip-unlocks-the-gamecube/)如果您正在寻找构建硬件插件来改进您使用的技术，无论是通过移除保护还是添加功能，现在都是最佳时机！

 [https://www.youtube.com/embed/NXqLMmGwJm0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/NXqLMmGwJm0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

