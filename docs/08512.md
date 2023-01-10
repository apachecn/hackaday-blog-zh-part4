# 通过超声波泄漏数据

> 原文：<https://hackaday.com/2020/12/06/leaking-data-by-ultrasound/>

人类的耳朵能够感知从大约 20 赫兹到 20 千赫兹的频率，至少在新的时候是这样。相应地，我们的音频硬件或多或少是针对这些频率而设计的。然而，在上边通常有一点额外的能力，[，[亚采克]显示可以利用它来过滤数据。](https://lipkowski.com/sonify/)

黑客利用了这样一个事实，即大多数计算机可以以高达 48 kHz 的采样率运行它们的声卡，由于奈奎斯特定理，这意味着它们可以输出高达 24 kHz 左右的频率——仍然在人类听觉范围之外。电脑和笔记本电脑也经常使用小型扬声器驱动器，能够很容易地产生这种频率的声音。通过使用一个简单的 Linux shell 脚本，[亚采克]能够让一台笔记本电脑通过超声波输出莫尔斯电码，[并且在 20 米之外只用笔记本电脑的内置麦克风就能接收到。](https://lipkowski.com/sonify/)

[亚采克]喜欢探索替代的数据渗透方法；他之前在树莓派上试验过以太网泄漏。当然，对于任何 airgap 攻击，真正的挑战通常是在没有现有远程管理员访问权限的情况下让远程机器运行渗透脚本。休息后的视频。

 [https://www.youtube.com/embed/MfOy_7g7fdI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/MfOy_7g7fdI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

