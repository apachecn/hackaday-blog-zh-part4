# Quadrivium EnsembleBot 是一项爱的工作

> 原文：<https://hackaday.com/2021/10/19/the-quadrivium-ensemblebot-is-a-labour-of-love/>

Quadrivium EnsembleBot 项目是旧学校乐器和现代 MIDI 控制世界的混搭。这些手工制作的乐器由一个小团队历时数年制作而成，看起来和听起来都非常棒。

电子方面的事情由一堆 Arduinos 和现成的模块处理，但这并不意味着设计没有经过深思熟虑，如果在某些地方比它可能更复杂一点。控制由 PC 通过 USB 向 Arduino 2560 发送命令来完成。第一个 Arduino 被称为主控制器，直接负责驱动打击乐器以及其他用简单螺线管打击的乐器。所有这些感性负载都通过光隔离器进行开关，以防止开关产生的任何噪声远离微控制器。四个 16 通道 GPIO 扩展器模块挂在 I ² C 总线上，以提供更多的光隔离输出，因为即使是 Arduino 2560 也没有足够的 GPIO 引脚可用。有许多仪器具有更复杂的控制要求，这些仪器通过 SPI 至 CAN 模块连接到专用从机 Arduinos。这些都处于不同的发展阶段，我们会密切关注。

其中一个更复杂的仪器是 PipeDream61，这是他们第二次尝试建造一个机器人管风琴。这是由 Teensy 提供的，因为他们认为 Arduino 在资源上有点太紧张了。这个器官有一个使用 ATTiny85 的温度控制器，以便进一步减轻主控制器的负担，并稍微简化开发。

另一个有趣的乐器是 [Robro](https://ensemblebot.quadrivium.dk/robro/) ，这是一个机器人[共鸣吉他](https://en.wikipedia.org/wiki/Resonator_guitar)，正如他们所说，尽管他们一直试图让它工作，但它仍在进展中。这里显然有相当多的控制复杂性，这就是为什么它需要这么多摆弄(嘿！)来让它工作。

这个项目绝不是独一无二的，最近我们已经介绍了用 MIDI 控制教堂风琴，以及整洁的 T2 Arduino 管弦乐队，但是 EnsembleBot 不仅仅是这样。

 [https://www.youtube.com/embed/jBWFsYhfKzY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/jBWFsYhfKzY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



谢谢你的提示！