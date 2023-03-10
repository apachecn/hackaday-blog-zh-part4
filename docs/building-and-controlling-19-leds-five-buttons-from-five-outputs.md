# 构建和控制 19 个发光二极管和 5 个按钮的 5 个输出

> 原文：<https://hackaday.com/2019/01/20/building-and-controlling-19-leds-five-buttons-from-five-outputs/>

数字在英语中已经够难了，但是[Sadale]决定更进一步，制造一个可以在 Toki Pona 中工作的计算器。结果就是 [Ilo Nanpa](https://sadale.net/58/ilo-nanpa-toki-pona-calculator---release-announcement-and-technical-details) ，一个用这种[合成最小语言](https://en.wikibooks.org/wiki/Toki_Pona)工作的令人敬畏的硬件计算器。这比你想象的要难一点，因为 Toki Pona 没有像英语这样的新拉丁语言那样的数字。相反，你把较小的数字组合成较大的数字。一个是万，两个是屠，但三个是万屠(1+2)。正如您所料，这使得处理和表示较大的数字变得有些复杂。

Ilo Nanpa 以一种非常优雅的方式解决了这个问题，并做了一些令人印象深刻的幕后工作。该计算器有 16 个 led，9 个按钮和一个滑动开关，但它们都是通过运行该设备的 STM8S001J3 控制器上的 5 个 IO 引脚来控制和读取的。

这是因为{ Sadale }在复用和 charlieplexing 方面做了一些出色的工作。多路复用是通过使用行和列来控制比控制输入更多的输出:这就是你可能正在阅读这篇文章的 LED 显示器可以通过几根电线来控制的方式。通过以肉眼看不到的速度切换这些行和列，您可以创建一个连续显示的幻觉。

Charlieplexing 更进一步，在单个连接上使用多个电压来进一步分离信号。Ilo Nanpa 巧妙利用分压器、led 的方向特性和多种电压水平，运行所有的 led，并通过五个引脚感应所有的按钮和滑块。这是一个非常整洁的设计，值得花一些时间查看[Sadale]写的对过程的精彩解释，看看它是如何完成的，并仔细研究设备的代码，看看他[如何将这一切编程到一个低功耗的芯片](https://github.com/SadaleNet/ilonanpa)。而且，当你阅读的时候，你可能会捡起几个 Toki Pona 的单词。塔瓦波纳！

 [https://www.youtube.com/embed/NgWCLg4H_4U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/NgWCLg4H_4U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

