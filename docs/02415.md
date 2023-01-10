# MiniITX 复古系统

> 原文：<https://hackaday.com/2019/03/16/the-miniitx-retro-system/>

有数百个现代的逆向计算项目将古代的 CPU 和芯片放在现代的环境中。来自[Lenore]的 neon 816 可能是我们见过的最令人印象深刻的项目之一。这是一个现代外形的经典系统，具有现代视频输出，融合在一个 MiniITX 主板上。

这台计算机的发电站是西部设计中心 W65C816 CPU。这是受人尊敬的 6502 CPU 的第二代，从 Commodore 64 到 Apple II 再到任天堂娱乐系统的所有产品都使用这种芯片。65816 *在启动时是* a 6502，直到你翻转寄存器中的一位，这时地址总线上的信号变得更加奇怪。[在](https://hackaday.com/2015/07/29/review-single-board-65c02-and-65c816-computers/)之前，我们已经看到了一些基于 65816 的单板计算机，8 位的家伙有一些想法[围绕这个 CPU](https://hackaday.com/2019/03/02/the-8-bit-guy-builds-a-16-bit-computer/) 建造一台计算机，但在可预见的未来，这方面的工作将陷入开发地狱。

值得注意的是，Neon816 将具有 DVI 输出(我猜技术上你可以通过连接器运行模拟信号)、PS/2 操纵杆输入、两个 Atari / Sega 操纵杆端口、MIDI 输入和输出、PC 风格的软盘连接器和 Commodore 串行总线。这是经典复古娱乐的大杂烩，全部集成在一个 MiniITX 主板上。

Neon816 的另一个关键特性是一个 FPGA，特别是一个用于视频和音频的晶格 XP2 8000 LUT 芯片。这与 1MB 的主 RAM(看起来像一个简单的 SRAM)和 128k 的 ROM 闪存相结合。里面还有一个 SD 卡可以存储。

现在，[Lenore]正在组装第一个原型板，我们迫不及待地想看到这个令人印象深刻的小系统生成的一些视频。