# 奇怪的输入和特殊的外设:在现代计算机上使用 Commodore 光笔

> 原文：<https://hackaday.com/2022/06/11/odd-inputs-and-peculiar-peripherals-using-a-commodore-light-pen-on-a-modernish-computer/>

如果你在 20 世纪 70 年代使用过计算机，你很有可能在某个时候使用过光笔:一种简单的输入设备，你可以在 CRT 屏幕上高亮显示文本、选择菜单选项或操纵图形对象。虽然在那个时代无处不在，但光笔在人机工程学的战斗中输给了不起眼的鼠标，并在 20 世纪 80 年代末几乎灭绝。触摸屏手写笔今天实现了类似的功能，但触摸屏幕不知何故与简单地指向屏幕感觉不一样。

因此，我们赞扬[Maciej Witkowiak]通过为 Commodore 64/128 光笔构建 USB 接口，将光笔带入 21 世纪的努力。其核心是一个 Arduino Micro Pro，它实现了 USB HID 协议，可以与任何现代计算机进行通信。它连接到传统的光笔以及计算机的模拟显示信号，并使用这些信号来计算视频同步脉冲和光笔输出之间的延迟。同步脉冲由 LM1881 从视频信号中提取，这是一款同步分离器芯片，熟悉模拟视频信号的人都很熟悉。

Arduino 根据测量的时间间隔计算光笔的位置，并将其报告给计算机，使用绝对定位模式，该模式也用于绘图板等设备。[Maciej]在下面嵌入的视频中演示了他的系统，在视频中，他用它来操作 X window 系统上的菜单。这是一个巨大的成功，尽管有一个问题:光笔只能在 CRT 显示器上工作，所以如果你想亲自尝试，你需要从存储中拖出一个大玻璃怪兽。

在[这个奇怪的游戏输入设备](https://hackaday.com/2015/06/15/a-revolutionary-input-device-30-years-too-late/)中，我们已经展示过 Commodore light pen。用分立 LED 矩阵制造的类似设备[很好地说明了光笔的工作原理。](https://hackaday.com/2014/07/09/light-pen-draws-on-led-matrix/)

 [https://www.youtube.com/embed/pBoyV9sNZWI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/pBoyV9sNZWI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[![Odd Inputs and Peculiar Peripherals Contest](img/4c1d0cbefc0219866bf706dbbac40818.png)](https://hackaday.io/contest/185414-odd-inputs-and-peculiar-peripherals)