# Micropython 和 C 一起玩更好

> 原文：<https://hackaday.com/2019/08/31/micropython-and-c-play-together-better/>

Python 是一种功能强大的通用语言，但有时它并不是最佳选择，尤其是当您在内存有限的嵌入式系统中工作时。对于这些情况，有时您可以使用 MicroPython，但是最好的语言可能是 C 或汇编语言。如果你真的很固执，像[amirgon]一样，并且真的希望 C 和 Python 能够很好地合作，你可以利用他的新工具[，它可以将任何 C 库带到 MicroPython](https://blog.littlevgl.com/2019-08-05/micropython-pure-display-driver#micropython-api-to-any-c-library) 。

作为如何使用该工具的一个例子，一个用于 ESP32 上的 ILI9341 的“纯 MicroPython”显示驱动程序，这意味着一切都在 MicroPython 中实现。[amirgon]想看看 Python 驱动程序与已经用 C 编写的驱动程序相比如何，并使用它来展示 MicroPython 绑定。该工具还自动将结构、联合、枚举和数组转换为 Python 对象，并提供了一种处理指针的方法，这是 Python 无法像 C 语言那样处理的。

[amirgon]希望这个工具通过消除 MicroPython 中缺少 API 和库的障碍，鼓励采用 Micropython。因为像这样的系统的大多数库都是用 C 编写的，所以用 Python 实现它们的方法肯定是强大的。[不久前](https://hackaday.com/2019/02/28/littlevgl-brings-gui-tools-to-micropython/)我们有一个用例，但这是一个更通用的解决这个编码障碍的方法。