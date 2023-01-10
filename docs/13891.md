# 奇怪的输入和特殊的外设:一个带有便捷布局屏幕的宏面板

> 原文：<https://hackaday.com/2022/06/11/odd-inputs-and-peculiar-peripherals-a-macropad-with-a-handy-layout-screen/>

宏键盘的想法很棒，它是一组可编程的键，可以执行频繁但复杂的任务。但是一旦被编程，用户如何跟踪哪个键做什么？为了从肮脏的、手写的粘性标签中拯救世界，这里有【Andreas Kä nner】和[Badger 2040 键盘](https://kaenner.de/badger-2040-keypad)——一个带有显示屏的宏键盘，可以显示使用 CircuitPython 完全可编程的键图信息。

它的核心是一个 [Pimoroni Badger 2040](https://shop.pimoroni.com/products/badger-2040?variant=39752959852627) 电子墨水屏幕和 RP2040 板，它位于一个 3D 打印的外壳中，该外壳又通过磁性附着在 3D 打印的键盘外壳上。里面是一个 I/O 扩展板，它是用导线连接到交换机上的。固件允许键盘本身的简单配置甚至扩展，并通过 USB 将其自身呈现给主机。甚至有可能在同一个设备上有多种不同的布局。

完整的细节可以在[他的网站](https://kaenner.de/badger-2040-keypad)上找到，而[所有的文件都在 GitHub 库](https://github.com/akaenner/Badger2040Keypad)里。如果这不能满足你对可定制输入的需求，那么[这不是我们向你展示的第一个宏键盘](https://hackaday.com/2022/03/18/modular-multi-input-macro-keypad-integrates-mouse-and-joystick/)。

[![Odd Inputs and Peculiar Peripherals Contest](img/4c1d0cbefc0219866bf706dbbac40818.png)](https://hackaday.io/contest/185414-odd-inputs-and-peculiar-peripherals)