# 军用规格键盘现在向 USB 致敬

> 原文：<https://hackaday.com/2020/02/27/mil-spec-keyboard-now-salutes-usb/>

当[easyjo]以低廉的价格买到这款 80 年代末的马可尼军用键盘时，他知道将它转换成 USB 并不容易——只是觉得值得。剧透:这些发光二极管不是 mod，它们是原生的。它们从四个角上的关键痕迹中获得有趣的形状。

[![](img/a1cd3dacd92381fade75227d1e35b440.png)](https://hackaday.com/wp-content/uploads/2020/02/kbd-chip.png) 尽管有像 WPNS HOLD 这样很酷的按键，而且控制键在它应该在的那一行，这个键盘看起来一点也不好玩。当然，这种键盘的要点不是舒适，而是一种可靠的输入设备，可以阻挡灰尘、汗水、液体和敌人。

这可能是为什么控制器嵌入到按键开关 PCB 的下侧，而不是生活在自己的板上。[easyjo]试图分析现有 26 针连接器的信号，但没有成功。

因此，一旦他能够解码矩阵，他就移除控制器芯片，并将行和列直接连接到 Arduino Leonardo。幸运的是，led 只是从电路板的正面为它们的列供电。

某些种类的军事剩余物资的可用性可以促成真正有趣的现代化项目，比如给一部野外电话增加几个罐子。

通过 [r/duino](https://www.reddit.com/r/electronics/comments/f8pdpf/i_converted_a_1980s_military_keyboard_to_usb_took/)