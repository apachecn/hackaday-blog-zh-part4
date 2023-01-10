# 由于强大的微控制器，在 CRT 上玩口袋妖怪

> 原文：<https://hackaday.com/2019/02/26/playing-pokemon-on-a-crt-thanks-to-a-powerful-microcontroller/>

如今，微控制器的功能非常广泛。有古老的 8 位微处理器，它一直存在，并勇敢地处理，一直到现代的 32 位处理器，具有先进的外设和大量的 RAM 和 ROM。如果你正在闪烁几个发光二极管或打开一个车库门，前者是好的。对于[贾里德]的想法，需要多一点马力。

[Jared]的项目最初是在 STM32F446RE 微控制器上进行复合视频输出的实验。利用 4 位电阻 DAC，该器件能够输出 NTSC 信号，利用中断和 nop 处理时序。硬件工作正常，并通过完整播放《星球大战:来自 SD 卡的新希望》进行了测试。

然后注意力转向为该平台创建一个 Game Boy 模拟器。在各种错误和边缘情况的许多障碍之后，事情开始工作，尽管很慢。口袋妖怪游戏 ROM 不适合微控制器有限的闪存存储，所以[Jared]实现了一个复杂的存储库切换方案。这与有限的计算资源相结合意味着游戏是可玩的，但仅限于 10 FPS。

进入 STM32H7。时钟速度提高了一倍以上，能够达到 856 DMIPS，而原来的芯片只有 225 DMI PS，一切都变得简单了。口袋妖怪现在以 60 FPS 的速度运行，内置的 DAC 大大改善了声音。DMA 子系统允许进一步提高性能，即使在调试模式下运行，性能也远远超过以前的硬件。

大多数微控制器的单价非常低，这表明一旦你在一个平台上挖掘出性能，通常会有更快的选择。正如 Sprite_TM 在 2016 年向我们展示的那样，在 ESP-32 上模仿 Game Boy 也是可能的。休息后的视频。

【感谢本的提示！]

 [https://www.youtube.com/embed/yKLkl-tMFnI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/yKLkl-tMFnI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/cA1a0taytvY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/cA1a0taytvY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

