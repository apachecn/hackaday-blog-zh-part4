# 一杆红外助手是一个伟大的初学者项目

> 原文：<https://hackaday.com/2022/07/13/one-shot-ir-helper-is-a-great-beginner-project/>

有时候你需要一个小工具来做一件非常简单的工作，并且做好。这个来自[Gregory Sanders]的一次性红外助手就是这样。

[Gregory]有一台电视不支持通电时自动打开。当你想让设备在不使用时硬关机以节省待机能耗时，这是令人沮丧的。因此，需要有一种方法在他的多显示器设置打开时向屏幕发送一个 on 信号。

一个简单的电路和一个 Pi Pico 配合使用。Pico 闪烁着红外 LED，喷射出必要的代码，告诉 TCL 品牌的电视打开。[Gregory]通过使用 Arduino 读取带有红外传感器的电视遥控器的输出，找出了代码。这里的关键是代码是用 MicroPython 编写的，使用了来自[Peter Hinch]的 IR 库。

现在，当[格雷戈里]打开他的装置时，红外发射器将触发电视打开。工厂里没有自动开机功能，这有点令人沮丧，但不管怎样，现在一切都正常了。如果你想反过来做这件事，考虑为跳舞的奶奶们使用的音箱制作一个 [TV-B-Gone](https://hackaday.com/2020/06/25/diy-tv-b-gone-is-a-ok/) 或[消音器](https://hackaday.com/2021/10/28/speaker-stun-gun-aims-to-combat-chinas-dancing-grannies/)！