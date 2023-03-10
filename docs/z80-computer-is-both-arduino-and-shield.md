# Z80 电脑既是 Arduino 又是 Shield

> 原文：<https://hackaday.com/2020/03/07/z80-computer-is-both-arduino-and-shield/>

Hackaday 上有很多 Z80 计算机版本，但是让它们与众不同的是你用它们做了什么。[Andrew]用他的 Z80 单板计算机从头开始写，使用 Arduino 标准接口作为它的 I/O。反过来，由于他需要一种简单的方法来对保存软件的闪存进行编程，以便在 Z80 上运行，他使用 Arduino Mega 作为调试器，使 SBC 本身成为 Arduino 屏障。

为 Z80 计算机使用这样一个通用的插头引出线，允许它与各种现成的 Arduino 屏蔽一起使用。这种兼容性是通过模拟数字转换器和 3.3 V 调节器实现的，模仿 Arduino Uno 中的引脚。GitHub 上的代码[包括对 Mega 从 Z80 接管总线作为全功能调试器的过程的广泛解释和演练。程序可以通过将汇编列表嵌入到 Mega 的草图中来加载，或者，一旦调试器启动，您也可以通过串行连接上传编译好的十六进制文件。](https://github.com/blackjetrock/z80_shield)

这不是安德鲁第一次出现在这里，他过去的项目也同样有趣。如果你需要[将苏联时代计算器的按键翻译成英文](https://hackaday.com/2019/12/13/3d-printer-and-cnc-make-this-russian-calculator-bilingual/)、[破解金相显微镜](https://hackaday.com/2017/10/01/hacking-a-metallurgical-microscope/)甚至[调查那噼啪作响的摩擦声](https://hackaday.com/2019/01/04/the-mystery-of-the-clacking-clanking-scraping-sound/)，你应该找他。