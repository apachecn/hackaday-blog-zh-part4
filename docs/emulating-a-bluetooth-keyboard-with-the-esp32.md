# 使用 ESP32 模拟蓝牙键盘

> 原文：<https://hackaday.com/2020/02/13/emulating-a-bluetooth-keyboard-with-the-esp32/>

大多数人将 ESP 系列微控制器与 WiFi 联系在一起，这是有道理的，因为它们已经成为快速轻松地让您的项目在线的首选解决方案。虽然 WiFi 功能可能是展会的明星，但 ESP32 也配备了蓝牙；我们只是没有看到人们经常使用它。如果您想在 ESP32 上开始使用蓝牙，[那么[Brian Lough]的这个简单的无线宏键盘将是一个很好的入门方式](https://github.com/witnessmenow/arduino-switcheroonie)。

从硬件的角度来看，这个项目非常简单。您只需将薄膜键盘连接到 ESP32 上的 GPIO 引脚。添加电池是一个不错的选择，你可能想把它放入某种外壳中，但作为概念验证，没有比这更简单的了。在这种情况下,[Brian]使用 TinyPICO 板，但您个人选择的 ESP32 版本也同样适用。

项目的其余部分都是软件，休息后[Brian]将在视频中为我们演示。ESP32 上有一个预先存在的蓝牙人机接口设备(HID)仿真库，但需要手动安装在 Arduino IDE 中。在那里，他演示了如何构建一个功能键盘，包括诸如一次发送多个虚拟键的技巧。

过去[我们已经看到 ESP32 被用来创建蓝牙游戏控制器](https://hackaday.com/2019/04/29/esp32-adds-bluetooth-to-gamecube-controllers/)，但是模拟键盘的能力显然提供了更多的灵活性。通过实际演示将这款低成本微控制器转变为无线输入设备是多么容易，我们有望看到更多利用该功能的项目。

 [https://www.youtube.com/embed/4sIkW7wogrE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/4sIkW7wogrE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

