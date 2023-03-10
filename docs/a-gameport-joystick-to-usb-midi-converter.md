# 游戏端口操纵杆到 USB-MIDI 转换器

> 原文：<https://hackaday.com/2022/02/24/a-gameport-joystick-to-usb-midi-converter/>

如今，现场音乐表演通常使用电子合成器和电脑，而不是传统的手工乐器。为了帮助他自己的表演，[alekappa]建造了一个特殊的接口，从操纵杆获取信号，并将其转换为通过 USB 传输的 MIDI 信息。

构建简单明了，使用一个小小的 LC 与一个简单的 gameport 操纵杆进行交互。有了一些简单的组件，只需要一点点去抖代码就可以很容易地读取操纵杆的输出，以确保操纵杆的按钮被准确读取。类似地，利用微控制器上的模数转换器读取模拟轴。

然后，这些数据被转换成控制变化、音符触发和力度级别，并通过 Teensy LC 的 USB 接口发送出去。模式开关可以快速改变系统的行为。该设备被包装在一个方便的外壳中，该外壳是从多年前的一个旧游戏端口到 USB 转换器中捕获的。

这是一个很好的项目，我们确信操纵杆可以让 alekappa 在舞台上的表演增加一个新的维度。我们也看到了其他伟大的 MIDI 控制器，从[针织键盘](https://hackaday.com/2021/06/30/mits-knitted-keyboard-is-quite-a-flexible-midi-controller/)到令人印象深刻的[口琴草堂。](https://hackaday.com/2020/01/29/harmonicade-is-a-high-scoring-midi-controller/)如果你正在建造自己的疯狂音乐剧，不要犹豫[给我们写信吧！](http://hackaday.com/submit-a-tip)