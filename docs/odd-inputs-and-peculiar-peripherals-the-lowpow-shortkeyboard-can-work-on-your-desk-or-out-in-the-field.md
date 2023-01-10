# 奇怪的输入和特殊的外围设备:低功耗的短键盘可以在你的桌子上或野外工作

> 原文：<https://hackaday.com/2022/06/28/odd-inputs-and-peculiar-peripherals-the-lowpow-shortkeyboard-can-work-on-your-desk-or-out-in-the-field/>

对于一些高级用户来说，普通键盘上的 100 多个按键不足以满足他们的日常任务。宏键盘是一种扩展输入能力的流行方式，有多少超级用户就有多少宏键盘。[Ulrich]的最新项目被称为[低功耗 E-Ink 短键盘](https://hackaday.io/project/185789-lowpow-e-ink-shortkeyboard-ble-wired-lorawifi)，这是一个美丽而精心记录的宏键盘设计，包括几个不同寻常的功能。

围绕 ESP32-S3 微控制器构建的短键盘具有九个可编程功能键，外加一个模拟操纵杆和一个旋转编码器。按键基于机械键盘中常见的樱桃 MX 红色类型，由微型 RGB LEDs 从下方照亮。中间一个大的电子墨水显示屏可以用来显示每个键的功能。

这很简洁，但真正让这款设备脱颖而出的是它的附加功能。其中之一是连接性:与主机 PC 的通信可以通过常规的 USB-C 电缆进行，但由于 ESP32 的内置无线功能，它还可以通过蓝牙低能耗甚至通过 WiFi 进行通信。甚至还有一个 868 MHz 的 LoRa 无线电，使它可以用作户外设备的遥控器。

这个短键盘可以用电池供电，这要归功于一个充电器芯片，每当 USB 电缆连接时，它都会保持锂电池充满电。智能电源管理系统确保键盘在电池供电时尽可能保持睡眠模式；根据[Ulrich]的计算，在不使用时，其电流消耗应降至 50 nA 左右。

键盘也有空间通过 I2C 连接环境传感器。这个想法是，该系统可以跟踪你办公桌上的空气质量，这是你可能会花很多时间的地方。我们还可以想象一些户外操作的用例，比如污染监测或者气象项目。

虽然短键盘的组装仍在进行中，但我们目前所看到的肯定是有希望的。渴望更多的宏键盘？看看[这个漂亮的建筑](https://hackaday.com/2020/04/16/software-shortcut-keyboard-registers-many-macros/)或者[这个可爱的 3D 打印的小模型](https://hackaday.com/2020/02/05/micro-macro-keyboard-makes-a-major-difference/)。

 [https://www.youtube.com/embed/PBEIaAEc3U4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/PBEIaAEc3U4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[![Odd Inputs and Peculiar Peripherals Contest](img/4c1d0cbefc0219866bf706dbbac40818.png)](https://hackaday.io/contest/185414-odd-inputs-and-peculiar-peripherals)