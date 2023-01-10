# 家酿流甲板踏板模拟真实的事情

> 原文：<https://hackaday.com/2022/07/14/homebrew-stream-deck-pedal-emulates-the-real-thing/>

踏板是控制电脑功能的好方法。你很少用脚做其他事情，所以它们可以处理一些任务，解放你的双手。[这款来自[DDRBoxman]的 Elgato Stream Deck 控制器就是这么做的。](https://github.com/DDRBoxman/picodeck)

[DDRBoxman]想要控制 Elgato Stream Deck，就像该公司出售的官方踏板一样。因此，一些黑客是有序的。将 Wireshark 与 Elgato 踏板配合使用有助于确定真实硬件的通信方法。

一旦协议确定下来，就只需要让 Raspberry Pi Pico 复制相同的功能了。在 tinyusb 库的帮助下，[DDRBoxman]成功地模拟了真正的 Elgato 设备。搭配 Adafruit 的 3D 打印脚踏开关设计，该项目功能齐全。

这些年来，我们已经看到了很棒的脚踏装置，从简单的微距装置到超级有用的活页乐谱翻页器(T2)。如果你一直在研究自己的输入设备，[一定要给我们写信！](http://hackaday.com/submit-a-tip)