# 通过 Twitter 访问 8 位 Atari

> 原文：<https://hackaday.com/2020/10/11/access-an-8-bit-atari-through-twitter/>

建造一台复古计算机，甚至是修复一台，是理解许多计算基础的好方法。不过，这可能需要很长时间和大量精力。幸运的是，有一个 Twitter 机器人可以让你体验一台旧的 8 位 Atari，甚至不需要启动模拟器。[只要把你的程序推送给机器人](https://twitter.com/atari8bitbot)，它就会输出结果。

该机器人由[Kay Savetz]创建，接受五种编程语言的程序:Atari BASIC、Turbo-Basic XL、Atari Logo、Atari PILOT 和 Atari Assembler/Editor，Atari Assembler/Editor 是这些机器上可用的低级汇编语言。该机器人本身运行在带有 Atari 800 仿真器的 Raspberry Pi 上，而不是原始硬件上，大概是因为在 Pi 上获得工作网络连接比在 80 年代的计算机上简单得多。Pi 运行一个 python 脚本，每两分钟轮询一次 Twitter，然后将代码交给仿真器。

[凯]的工作不仅限于阿塔里斯，虽然。还有一个面向所有苹果粉丝的 Apple II BASIC 机器人，它可以响应用 AppleSoft BASIC 编写的程序。虽然[构建自己的复古系统](https://hackaday.com/2017/05/13/a-mini-itx-atari-800/)或[在其他硬件上模仿一个](https://hackaday.com/2016/12/19/portable-apple-ii-on-an-avr/)是一个很好的练习，但有这样的工具允许操作复古计算机而无需我们自己做任何脏活也是很棒的。