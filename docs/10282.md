# 神经网络模拟任何吉他踏板，售价 120 美元

> 原文：<https://hackaday.com/2021/05/30/neural-networks-emulate-any-guitar-pedal-for-120/>

众所周知，吉他手的敏锐度可以通过踏板的大小来准确衡量——踏脚转盘越多，演奏者越优秀。当你可以有许多只做几件事的盒子时，为什么要有一个能做所有事的盒子呢？

玩笑归玩笑，用一个盒子代替整个踏板系列的想法并不新鲜。标准的老式踏脚转盘是一种模拟事物，使用滤波器和放大器的组合来实现某种声音。一些现代多效果处理器使用旧踏板的软件模型来复制它们的声音。这些数字踏板自 90 年代就已经出现，但没有一个像 NeuralPi 项目一样。刚刚由[GuitarML]发布的 NeuralPi 需要大约 120 美元的硬件(包括——你猜对了——一个树莓派),并将其转化为完美的踏板。

这里的关键当然是神经网络。NeuralPi 的核心 LSTM 可以在任何踏板上进行训练，以准确再现其声音，由于 [Elk Audio OS](https://elk.audio/) ，它甚至可以以令人难以置信的低延迟做到这一点(它甚至为马特·贝拉米的 synth 吉他提供动力，正如在*缪斯*的模拟理论世界巡演中使用的那样)。训练模型的结果是一个 VST3 插件，这是一种描述音频效果的流行格式。

这不是我们第一次看到来自[GuitarML] 的一些非常酷的东西，它也让人回想起我们去年看到的 LTSpice 中的一些[甜蜜踏板模拟](https://hackaday.com/2020/10/29/rockin-out-in-ltspice-simulating-classic-guitar-pedals/)。我们迫不及待地想看到这个项目继续发展——随着时间的推移，看到一个光滑的用户界面会很棒，或者也许有人会设计一个很酷的外壳，带有一些旋钮和一个真正的用户输入踏板！

感谢[Mish]的提示！

 [https://www.youtube.com/embed/_3zFD6h6Wrc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_3zFD6h6Wrc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

