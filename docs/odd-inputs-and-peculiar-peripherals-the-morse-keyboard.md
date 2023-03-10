# 奇怪的输入和特殊的外围设备:莫尔斯键盘

> 原文：<https://hackaday.com/2022/06/14/odd-inputs-and-peculiar-peripherals-the-morse-keyboard/>

当涉及到将文本输入转换成电子形式时，最新的键盘使用 USB 进行有线接口，而最古老的莫尔斯键使用单导线。这两个人会见面吗？对马修·斯帕克斯来说，答案是肯定的，他的“[Gadget](https://hackaday.io/project/184702-morse-code-usbhid-interface-the-gadget)Morse-to-USB HID 接口可以将莫尔斯键呈现给电脑，就像它是一个 USB 键盘一样。

它的核心是一个 Seeduino Arduino 克隆体，在这个克隆体上，Morse 键摇动一个 pin，它通过软件的广泛魔力识别键入的字符，并将其转换为计算机的 USB 按键。因此，这是一个令人惊讶的简单项目，与 Arduino 代码相比，文章花费了更多的时间来宣传载波艺术。

莫尔斯既是一种手工艺术形式，也是通过拥挤的无线电波段进行通信的有效手段，还是一种时代错误，这可能解释了它在无线电业余爱好者中的持续吸引力。我们不确定有多少键盘战士会在这个项目中切换到单键，但我们可以看到它可能是一个有用的学习辅助工具，也是一个非常快速的输入方法。

莫尔斯以前在这里的许多项目中出现过，不仅仅是在这个辅助莫尔斯键盘中。

[![Odd Inputs and Peculiar Peripherals Contest](img/4c1d0cbefc0219866bf706dbbac40818.png)](https://hackaday.io/contest/185414-odd-inputs-and-peculiar-peripherals)