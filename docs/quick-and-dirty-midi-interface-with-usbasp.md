# 快速和肮脏的 MIDI 接口与 USBASP

> 原文：<https://hackaday.com/2018/11/04/quick-and-dirty-midi-interface-with-usbasp/>

【Robson Couto】最近发现自己正在做的一个项目需要 MIDI 接口，但不想买一个只是为了用一次；我们都经历过。作为一个富有创造力的人，他决定不仅要利用手头的零件，而且要在一个下午完成。真正符合我们心意的黑客。

[![](img/b1e721b10f50c1f5ea8a0714751b6283.png)](https://hackaday.com/wp-content/uploads/2018/11/usbmidi_detail.png) 在网上四处搜索，他找到了使用 ATtiny 微控制器作为使用 V-USB 的 MIDI 接口的文档。他认为让这个项目在他在身边的众多 USBASP 程序员中的一个上运行应该不会太难，并开始更新代码。

最初是为 ATtiny2313 编写的，[Robson]首先必须改变引脚配置，以便它可以在 USBASP 中的 ATmega8 上工作，并且还将 USB-V 实现更新到最新版本。随着代码的更新，他将其中一个 USBASP 适配器与另一个适配器连接起来，并在 J2 接头上放置了一个跳线，从而对它们进行了编程。

他把软件整理好了，但还有一些硬件工作要做。为了给 MIDI 设备提供隔离，他在一块 perf 板上利用 6N137 光隔离器和几个无源元件组装了一个小电路。它并不漂亮，但确实适合 USBASP 上的编程连接器。他[本可以启动他的 PCB CNC](http://hackaday.com/2018/09/12/turning-a-cheap-engraver-into-a-decent-pcb-mill/) ,但他认为对于这样一个简单的电路板来说有点大材小用了。

[Robson]指出，他还没有用他的适配器实现 MIDI 输出，但是如果你的项目需要它，代码和芯片完全有能力实现它。找到连接到编程器 TX 引脚的原理图是留给读者的练习。

如果你的零件箱里没有 USBASP，我们已经看到过一个非常相似的技巧[在过去用 Arduino 克隆完成](https://hackaday.com/2017/09/26/cheap-diy-midi-to-usb-adapter/)。