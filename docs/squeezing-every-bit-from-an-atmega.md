# 从自动取款机中榨出每一点

> 原文：<https://hackaday.com/2020/12/26/squeezing-every-bit-from-an-atmega/>

虽然 ATMega328 对于微控制器来说是“巨型”的，但它仍然是一个相当有限的平台。它有足够的 I/O 和工作内存来完成大多数任务，但[thorlancaster328]组装的这款战舰游戏确实扩展了这个小小芯片的能力。通常情况下，战舰游戏不会那么复杂，但这款游戏有音频，LED 显示屏，还可以播放一段精彩的 Nyan Cat to boot，[这真的让 Atmel 芯片通过了测试](https://www.reddit.com/r/arduino/comments/kesrb6/working_on_my_arduino_battleship_game_got_it/)。

音频通过一个 512 字节的缓冲区播放，当微控制器处理其他进程时，一个中断触发微控制器何时填充缓冲区。12×12 LED 显示屏也通过一个移位寄存器进行馈送，该移位寄存器由与音频相同的中断触发，由于该构建使用了如此多的移位寄存器，因此微控制器实际上可以输出四个独立的显示屏(两个播放器，每个都有一个镜头显示屏，一个船只显示屏)。它也将最终支持战舰游戏的玩家对电脑模式，并且也有一个模式，它玩 Nyan cat 只是为了展示它自己的能力。

我们对这个小型微控制器所做的大量工作印象深刻，这主要归功于它的创造者[thorlancaster328]的代码优化。如果有足够的兴趣，他还说他也会提供源代码。在此之前，一定要看看另一种方式[将小型微控制器推向极限](https://hackaday.com/2012/12/27/overclocking-microcontrollers/)。

感谢[thinker]的提示！