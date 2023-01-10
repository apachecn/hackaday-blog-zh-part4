# 一个受创世纪启发的合成器，与菲尔·柯林斯毫无关系

> 原文：<https://hackaday.com/2019/01/25/a-genesis-inspired-synthesizer-that-has-nothing-to-do-with-phil-collins/>

Chiptune 是一种音乐类型，通过使用早期游戏控制台中的基于芯片的声音合成器来创建音乐。Commodore 64 古老的 SID 芯片和 Game Boy 音响系统是现场最受欢迎的。然而，世嘉 Genesis 在视频游戏 chipmusic 时代结束时走了一条不同的道路，包装了 YM2612 FM 合成芯片，以提供丰富的低音和灼热的独奏。[[Thea]一直是这些 90 年代电音的粉丝，因此决定建造 Genesynth。](https://blog.thea.codes/genesynth-a-sega-genesis-inspired-synthesizer/)

synth 最初只允许播放现有的视频游戏分数，但随着[Thea]将该项目从试验板到原型板再到定制的 PCBs 从动画作品到启动，它的功能已经得到了扩展。synth 使用 Teensy 3.5 作为大脑，通过 USB 接口使 synth 能够接收来自音乐软件的 MIDI 命令。所有的参数都暴露在界面上，并且[【Thea】有几个视频展示了在 Ableton Push 控制下的 Genesynth。](https://twitter.com/theavalkyrie/status/1056783107196473344?ref_src=twsrc%5Etfw%7Ctwcamp%5Etweetembed%7Ctwterm%5E1056783107196473344&ref_url=https%3A%2F%2Fblog.thea.codes%2Fgenesynth-part-4-cleaning-up-the-noise-in-synth-audio-amplifier%2F)

凭借 FM 合成引擎，YM2612 的声音功能与大多数 chiptunes 完全不同。FM 合成没有经典的加法合成那么直观，[，但我们仍然看到它不时出现](https://hackaday.com/2018/06/07/vaporwave-for-the-parallel-port/)。