# 新零件日:一个 64 位 RISC-V CPU，树莓派帽子形状

> 原文：<https://hackaday.com/2019/05/24/new-part-day-a-64-bit-risc-v-cpu-in-raspberry-pi-hat-form/>

在过去的几年里，开源 RISC-V 微处理器已经从仅存在于 FPGAs 上发展到真正的硅芯片上，现在你可以买到一个拥有你想要的所有功能的 RISC-V 微处理器。有一个来自中国的有趣的芯片叫做 Sipeed M1，它有一个双核 RISC-V 内核，运行速度为 600MHz，一堆 I/o，因为是 2019 年，还有一个神经网络处理器。我们以前见过这种芯片，但现在 Seeed Studios 将它作为树莓皮帽子出售。它是 Pi 的附加板，还是独立的东西？谁知道呢。

这款名为 Grove AI Hat for Edge Computing 的主板是围绕 Sipeed MAix M1 人工智能模块和 Kendryte K210 处理器构建的。这是一款双核 64 位 RISC-V 芯片，显然是本次展会的明星。除了这个芯片，您还可以获得一些用于数字 I/O、I2C、PWM 和 UART 的 Grove 接口。有一个 USB C 型电源(终于我们摆脱了 USB 微型电源插头)，当然还有一个 40 针树莓 Pi 型插头。

该板本质上是 Sipeed M1 芯片的分线板，这是自去年年底推出以来我们见过的最有趣的新型微控制器之一。这里有很多功能，人们已经在这个芯片上模仿任天堂娱乐系统[并取得巨大成功](https://hackaday.com/2019/03/14/nes-on-risc-v/)。这种芯片的问题是，除了制作自己的分线板，没有太多的选项来快速启动和运行它。这是解决这个问题的方法。至少它是一个带电源的板上的 Sipeed 芯片，它也是一个可以通过 Linux 和 Raspberry Pi 访问的协处理器。