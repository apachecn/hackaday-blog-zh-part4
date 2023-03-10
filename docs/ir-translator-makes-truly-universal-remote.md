# 红外翻译使真正的通用遥控器

> 原文：<https://hackaday.com/2022/02/10/ir-translator-makes-truly-universal-remote/>

如果你有很多设备都有自己的遥控器，通用遥控器是一个方便的工具。将它们全部合并到单个设备中会减少混乱和挫折，但是它们通常不是真正“通用的”,因为它们中的一些可能不支持已经制造的每个红外设备。如果你处于那种情况[，如果你手头有一个微控制器和几个红外发光二极管，就有可能制造一个真正通用的遥控器来代替](https://github.com/mattcuk/IRtranslator)。

这就是[Matt]发现自己的亚马逊 Fire TV 设备控制功能不支持他的扬声器型号时的情况。为了解决这个问题，他编写了一个 Arduino 来翻译遥控器的红外代码，并向扬声器输出一组兼容的代码。这需要一个红外光电二极管和一个红外发光二极管，但除了遥控器和相关设备的代码之外，几乎没有其他东西。随着所有的设置和编程进入 Aruino，[Matt]的遥控器离真正的“通用”又近了一步。

虽然[Matt]能够利用 Arduino 库中的现有代码，但也可以通过将遥控器指向光电二极管并对微控制器进行编程来捕获所需的代码，从而手动捕获所需的代码。[Matt]在调试该项目时使用了 Raspberry Pi 来完成这一任务，但我们也看到过类似的构建使用这种方法，其中[使用 ESP8266 通过其红外遥控功能](https://hackaday.com/2019/06/11/smarten-up-your-air-conditioning-with-the-esp8266/)来控制空调。

 [https://www.youtube.com/embed/rTCGy0bqljE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/rTCGy0bqljE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

