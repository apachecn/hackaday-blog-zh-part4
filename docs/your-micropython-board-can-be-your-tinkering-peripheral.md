# 您的 MicroPython 板可以是您的修补外设

> 原文：<https://hackaday.com/2022/08/10/your-micropython-board-can-be-your-tinkering-peripheral/>

[Brian Pugh]分享了一个同时在桌面 Python 和 MicroPython 上运行的很酷的新项目——[Belay 库。](https://github.com/BrianPugh/belay)该库允许您从 Python 代码无缝控制 MicroPython 设备，与模拟/数字小饰品、伺服系统、新像素和显示器等现实世界的事物进行交互，而无需创建自己的固件或 API。

你需要一个串行连接的 MicroPython 板，甚至一个 ESP8266 也可以。然后，您可以[用 MicroPython 编写的函数点缀您的 Python 代码](https://github.com/BrianPugh/belay/blob/main/examples/01_blink_led/main.py)，并在您需要连接的设备做某事时调用它们——将项目的整个逻辑保持在一个设备中。【Brian】提供了[相当多的例子，](https://github.com/BrianPugh/belay/tree/main/examples)甚至是更复杂的东西比如[显示器。毫无疑问，它有局限性，但这看起来是黑客武器库中的一个强大工具。](https://github.com/BrianPugh/belay/blob/main/examples/07_lcd/main.py)

读者可能会想起一个名为 Firmata 的 Arduino 库——[这是一种古老的连接方式。我们之前也报道过](https://hackaday.com/2010/01/16/developing-physical-controllers-for-the-uninitiated/)[一个做类似事情的 Pi Pico 固件](https://hackaday.com/2021/04/18/bridging-the-pc-and-embedded-worlds-with-pico-and-python/)，它甚至有一个分线板来满足你所有的实验需求！

 [https://www.youtube.com/embed/wq3cyjSE8ek?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/wq3cyjSE8ek?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

