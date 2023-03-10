# MIDI 同步您的 Eurorack 构件的简单方法

> 原文：<https://hackaday.com/2019/01/03/an-easy-way-to-midi-sync-your-eurorack-build/>

Eurorack 合成器的构建因很多事情而闻名；简单不一定是其中之一。然而，并不是模块化合成器构建的所有东西都必须非常复杂，一团乱麻，或者难以理解。[little-scale]已经建立了一个整洁的模块，可能会在您的设置中找到一个位置——[半音阶鼓门同步。](https://little-scale.blogspot.com/2018/12/chromatic-drum-gate-sync.html)这个方便的小设备基于 Teensy，并使用其 USB MIDI 库使同步硬件变得轻而易举。

该设备有 12 个通道，每个通道响应一个 MIDI 音符。“音符开”消息用于将门设置为高电平，而“音符关”消息用于再次将其设置为低电平。这允许在模块化设置中非常精细地控制门。该设备还可以输出由 USB MIDI 时钟控制的各种同步信号，这有助于使您的模块化机架与其他数字控制合成器保持同步。

这是一个支持[小规模]通常审美的建筑——干净整洁，注重紧凑。在 Github 上[可以找到构建自己的工具所需的所有细节。](https://github.com/little-scale/eurorack/tree/master/chromatic_drum_gate_sync)

我们以前已经看到过(小规模)和微小硬件的碰撞——[这台设备同时播放 8 个 SEGA 的声音芯片。](https://hackaday.com/2018/01/08/eight-segas-singing/)