# 迷你无线热敏打印机获得 Arduino 库(和 MacOS 应用程序)

> 原文：<https://hackaday.com/2021/09/21/mini-wireless-thermal-printers-get-arduino-library-and-macos-app/>

[Larry Bank]的用于在 BLE(蓝牙低能耗)热敏打印机上打印文本和图形的 Arduino 库具有一些出色的功能，可以尽可能轻松地将无线打印作业发送到许多常见型号。这些打印机体积小，价格便宜，而且是无线的。这是一个很好的组合，使它们对那些受益于打印硬拷贝的项目很有吸引力。

![](img/555c3cb86baaa588f84a13880c3e950f.png)

它也不局限于简单的默认文本。使用 [Adafruit_GFX 库](https://github.com/adafruit/Adafruit-GFX-Library)风格的字体和选项可以完成更好的输出，它将格式化的文本作为图形发送。你可以在[这本简明扼要的功能列表](https://github.com/bitbank2/Thermal_Printer/wiki/Public-API)中读到关于这个图书馆能做什么的所有内容。

但是[拉里]并没有就此止步。在试验微控制器和 BLE 热敏打印机的同时，他还想探索从他的 Mac 直接使用 BLE 与这些打印机对话。 [Print2BLE](https://github.com/bitbank2/Print2BLE) 是一个 MacOS 应用程序，允许将图像文件拖到应用程序的窗口中，如果预览看起来不错，打印按钮会让它作为 1-bpp 抖动图像从打印机中出来。

小型热敏打印机有助于整洁的项目，就像这个改装的宝丽来相机，现在这些小型打印机既无线又经济，在这样一个图书馆的帮助下，事情只会变得更容易。当然，如果这一切开始看起来有点太容易，人们总是可以通过使用等离子体将*热敏*放回热敏打印[，而不是](https://hackaday.com/2020/08/08/print-with-plasma/)。