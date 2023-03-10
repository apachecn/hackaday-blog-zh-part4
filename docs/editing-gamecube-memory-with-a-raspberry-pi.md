# 用树莓 Pi 编辑 GameCube 内存

> 原文：<https://hackaday.com/2018/12/05/editing-gamecube-memory-with-a-raspberry-pi/>

[James]已经使用 GameCubes、模拟器和 *Animal Crossing* 有一段时间了，虽然模拟器已经足够了，但他想在真正的硬件上玩。这意味着他需要写入 GameCube 存储卡。虽然有几个选项可以做到这一点，但它们要么需要一个 Wii，要么需要十年来都没有生产的硬件。解决这个问题的显而易见的方法是对 GameCube 存储卡[进行逆向工程，用树莓 Pi](https://jamchamb.github.io/2018/12/03/gamecube-memory-card-raspi.html) 读写内存。

每个游戏机都有数量惊人的非官方文档，而且[James]偶然发现了一个 GC-Forever 论坛帖子，描述了 GameCube 存储卡内的电信号。有标准的电源和接地焊盘，以及阿迪、DO、CS、Clk 和一个 INT 引脚。[詹姆斯]打破了磁线，并焊接了一个引脚头这些卡。然后用 Salae 逻辑分析仪捕捉数据，你瞧，它看起来就像一个标准 SPI 协议。

随着底层协议的制定，[James]查阅了另一份 GameCube 文档以获得 SPI 总线允许的主要功能。例如，“读取块”从 0x52 和地址偏移量开始。树莓 Pi 上的一点点 Python 意味着[詹姆斯]可以读写整个 GameCube 存储卡。现在代码有点粗糙，[但是所有的工作都是可用的](https://github.com/jamchamb/gc-memcard-adapter)如果你想编辑你的*动物穿越*保存一个树莓派。

这项工作是在[James]之前的工作之后进行的，即让[进入*动物穿越*](https://hackaday.com/2018/06/13/unlocking-animal-crossings-debug-mode/) 的调试菜单，允许他将物品添加到他的库存中。有了这一最新进展，我们将 Raspberry Pis 直接插入 GameCube 只是时间问题。