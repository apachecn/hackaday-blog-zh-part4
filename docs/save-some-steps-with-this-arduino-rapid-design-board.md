# 使用 Arduino 快速设计板节省一些步骤

> 原文：<https://hackaday.com/2018/07/28/save-some-steps-with-this-arduino-rapid-design-board/>

我们都很熟悉目前可用的各种 Arduino 开发板，我们看到一个又一个项目连接到 Nano 或 Uno 上。当然，这并没有什么错，但有些爱好者希望超越将电线插入插头插座的范围，将微控制器直接构建到他们的项目中。这时，人们通常会了解到开发板不仅仅是将微控制器线路连接到接头，而且开发自己的设计意味着包括所有支持电路。

为了使过渡更容易，[Sean Hodgins]已经提出了一种简单的 Arduino 兼容模块，可以直接焊接到 PCB 上。该模块基于 Atmel SAMD21 微控制器，被称为“HCC 模块”，用于电镀半圆形城堡，便于焊接。该模块具有 16 条 GPIO 线、6 个 ADC、一个 3.3 V 板载稳压器和一个复位按钮，具备启动所需的一切——只需设计一个具有正确焊盘布局的 PCB，焊接上它，并用电路环绕它。编程是在熟悉的 Arduino IDE 中完成的，因此您可以快速启动并运行。[Sean]有一个 Kickstarter 模块，但他也在[将其作为开源](https://github.com/IdleHandsProject/samd_hcc_mod)发布，所以你可以像他在下面的视频中一样自由地焊接自己的模块。

这当然不是第一个可以直接焊接到 PCB 上的开发模块，但我们喜欢这种设计，并且可以看到它将如何简化设计。[Sean]之前给我们展示了很多构建，比如[这支神经网络机器人大军](https://hackaday.com/2017/11/21/prototyping-making-a-board-for-and-coding-an-arm-neural-net-robot/)，所以他毫无疑问会很好地利用这些模块。

 [https://www.youtube.com/embed/7S2FcrVHBxY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/7S2FcrVHBxY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

