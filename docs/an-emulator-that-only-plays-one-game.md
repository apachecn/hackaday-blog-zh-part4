# 只玩一个游戏的模拟器

> 原文：<https://hackaday.com/2021/06/07/an-emulator-that-only-plays-one-game/>

[本恩·史密斯]之前已经实现了一个 GameBoy 彩色模拟器，但决定[制作一个新的模拟器，只玩一个叫做 pokegb](https://binji.github.io/posts/pokegb/) 的游戏。这个游戏当然是广受欢迎的口袋妖怪蓝色版。虽然这个模拟器可以玩其他 GameBoy 游戏，但它的实现方式是只支持 Pokemon Blue 使用的操作码和功能。也许更令人惊奇的是，这个完整的模拟器只有 582 行 C++(使用 SDL 进行图形和输入)。还有一个模糊版本，只有 68 行，形状是三个口袋球。pokegb 的所有代码都可以在 GitHub 上找到。

[Ben]详细列出了处理器、内存、图形单元(PPU)的每个操作码，以及它如何与现代操作系统交互。我们喜欢一个接一个地实现每个操作码，并逐渐看到仿真器在 ROM 中走得越来越远的想法。唯一明显缺少的特性是声音，这需要大量的代码来正确模拟。

如果你有兴趣深入了解 Gameboy 颜色中的音频芯片，[Ken Shirriff] [已经为你做了研究](https://hackaday.com/2020/06/27/comparing-bare-silicon-on-two-game-boy-audio-chips/)。