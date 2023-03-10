# 为您的 Arduino 添加一系列 8 位处理器

> 原文：<https://hackaday.com/2019/04/14/add-a-host-of-8-bit-processors-to-your-arduino/>

通常，当我们给你带来一个逆向计算设计的消息时，它将围绕一个单一的处理器。其核心将是 6502、Z80，或者可能是 6809。将会有许多支持芯片，一些内存如 RAM 或 ROM，以及一堆接口。[Erturk Kocalar]为 Arduino Mega 开发的[retro Shield 项目打破了所有这些规则，因为它支持所有三种经典处理器，没有支持芯片，没有内存，除了到 Mega 的 shield 连接之外没有外部接口。到底是怎么回事！](https://hackaday.io/project/164556-retroshield-for-arduino-mega)

仔细观察会发现，该项目是一套使用 Mega 的能力来模拟所有支持芯片和外围设备的屏蔽，你会在原始硬件上看到。虽然拥有一个支持所有三个 CPU 的主板令人印象深刻，但事实上每个 CPU 都有一个 PCB。但是，对于那些对 8 位处理器感兴趣的人来说，这并没有降低这个项目的兴趣，因为重点变成了软件，而不是寻找停产的硅。

到目前为止，有一些有限的演示软件，他的网站详细介绍了所需的接口和代码。Arduino 只能在软件中以 95kHz 的速度为 8 位 CPU 计时，这对那些熟悉 20 世纪 80 年代家用电脑的人来说可能听起来有点低，但最好把这当成一个实验平台，放弃玩*精英*的梦想。如果不可能的硬件是你的囊中之物，让 8 位机器访问 Arduino shields 将是一个令人兴奋的前景。

如果这引起了你的兴趣，你可能还想看看[4 美元的 Z80 单板计算机](https://hackaday.com/2018/07/28/the-4-z80-single-board-computer-evolved/)，它也有类似的特点。