# 家酿电路探索模数转换的奥秘

> 原文：<https://hackaday.com/2021/10/08/homebrew-circuit-explores-the-mysteries-of-analog-to-digital-conversion/>

当涉及到将模拟世界的信号输入我们的计算机时，我们大多数人都不太考虑硬件是如何工作的。但事实证明，有很多方法可以解决模数转换的问题，而[构建自己的自制逐次逼近型寄存器 ADC](https://hackaday.io/project/181826-homemade-successive-approximation-register-adc) 是消除一些神秘感的好方法。

从他对该项目的描述来看，很明显[Mitsuru Yamada]并不打算构建一个实用的 ADC，而是更感兴趣的是通过开发自己的 ADC 他能学到什么。逐次逼近型寄存器 ADC 的工作原理是在其输入范围内快速循环所有可能的电压电平，最终在该时刻锁定输入信号的电压，并输出其数字表示。下面的视频直观地展示了 SAR ADC 的工作方式，使用示波器显示内部 R-2R DAC 的输入电压和输出。该 ADC 的输入范围为 0 V 至 5 V，分辨率为 7 位，采样保持和比较器部分仅使用常见的 74xx 系列逻辑芯片和几个容易获得的模拟器件。和往常一样，他的一个项目，建造质量和工艺是无可挑剔的。

我们喜欢这类项目，这些项目仅仅是为了享受建造东西和学习它如何工作的乐趣。对于[山田先生]的更多项目，请查看[他的基于 6502 的 RPN 计算器](https://hackaday.com/2020/11/17/another-kind-of-bare-metal-6502-computer-powers-rpn-calculator/)，或者本应是的串行终端[。](https://hackaday.com/2020/12/08/a-portable-serial-terminal-that-should-be-from-the-1970s/)

 [https://www.youtube.com/embed/lxwAKFijk50?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/lxwAKFijk50?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

