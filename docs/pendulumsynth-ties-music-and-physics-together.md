# 钟摆合成器将音乐和物理联系在一起

> 原文：<https://hackaday.com/2022/02/17/pendulumsynth-ties-music-and-physics-together/>

许多音乐家都熟悉节拍器，这是一个钟摆，负责产生有节奏的滴答声，以保持一个人在固定时间内的表演。有了 PendulumSynth，[mrezanvari]采用了相同的基本钟摆[，但以完全不同的音乐方式使用它](https://hackaday.io/project/182341-pendulumsynth)。

该构建依赖于一个 10 英寸的塑料球作为钟摆的加权端，填充有 STM32F411CE BlackPill 板、BNO085 IMU 和用于发送数据进行外部处理的 nRF 无线电模块。钟摆的运动被转换成 MIDI 数据或 CV，输出到处理实际产生输出声音的音乐硬件。

该系统以多种模式运行。重力模式输出连续的 MIDI 数据和相对于钟摆连续运动的 CV，而 DIV3 模式跟踪钟摆的运动并输出 3 个相应的常规触发点。

钟摆直观的物理特性和其巨大的尺寸相结合，构成了一场迷人的音乐展览。[我们之前也看过其他一些很棒的音乐装置作品](https://hackaday.com/2021/08/22/esp32-is-the-brains-behind-this-art-installation/)。休息后的视频。

 [https://www.youtube.com/embed/r7tXlfV4hvE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/r7tXlfV4hvE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

