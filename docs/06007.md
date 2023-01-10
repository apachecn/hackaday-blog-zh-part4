# 开源一代的 NES 主板

> 原文：<https://hackaday.com/2020/03/22/a-nes-motherboard-for-the-open-source-generation/>

随着 8 位电脑游戏黄金时代的原始硬件变得有点过时，让它继续存在已经成为爱好者关心的事情。对于当时的许多主要平台来说，已经有了一系列的再制造零件，现在多亏了[Redherring32],轮到 NES 控制台了。

[OpenTendo 是原始前置任天堂娱乐系统主板](https://github.com/Redherring32/OpenTendo)的完全开源替代品，使用原始或售后市场任天堂 CPU 和 PPU 芯片，以及其他仍然容易获得的组件。它没有整合任天堂的 CIC 锁定芯片——德鲁·利特雷尔(Drew Littrell)写了[一篇关于该安全功能如何工作的伟大文章](https://hackaday.com/2018/10/22/that-time-atari-cracked-the-nintendo-entertainment-system/)——但如果你真的需要真实性，也有 [NullCIC](https://github.com/Redherring32/NullCIC) 项目可以模拟该组件。

这是一个有趣的逆向工程练习，也是一个在芯片层面观察 NES 的机会。此外，对于任天堂头，它提供了 KiCAD 格式的所有组件足迹和原理图项目。会建很多吗？鉴于 NES 是当时最畅销的游戏机，应该不会缺少原件，但这绝不意味着投入到这个项目中的努力无效。由于这样的工作，在未来的几十年里，某个地方将会有 NES 游戏机在运行，简单地记住，你不需要在插槽中吹气来使它工作！