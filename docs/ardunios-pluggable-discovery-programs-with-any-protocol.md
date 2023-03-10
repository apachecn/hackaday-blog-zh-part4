# Arduino 的任何协议的可插拔发现程序

> 原文：<https://hackaday.com/2019/05/08/ardunios-pluggable-discovery-programs-with-any-protocol/>

第一个 Arduino 是串行的，十五年来，这一直是将代码上传到 Arduino 板的默认方式。2008 年增加了对内嵌编程器的支持，后来又增加了端口检测。Arduino IDE 的最新版本增加了一些新东西:[可插拔发现](https://www.pjrc.com/arduino-pluggable-discovery/)。现在 Arduino IDE 支持任何协议。

这个功能是[保罗·斯托佛雷根]的创意，他是 Teensy 的创造者。如果你曾经使用过 Teensy，你会记得 Teensyduino 应用程序用来上传代码到板上。Teensy 使用 HID 协议而不是串行协议进行上传。在致力于改进 Teensy 和 Arduino IDE 之间的集成之后，[Paul]声明扩展 DiscoveryManager。在与 Arduino 开发人员进行了一些讨论之后，这个特性被添加到大约一个月前发布的 Arduino 1.8.9 中。

可插拔发现存在一些问题，最重要的是它还不存在于 Arduino 命令行界面中(是的，它也存在)。如果你想为开源做贡献，这将是一个不错的选择。

有了正确的 JSON 和配置，现在理论上可以将 Arduino IDE 扩展到任何类型的协议。这意味着(再次，理论上)，有可能更新你的 DIY MIDI synth over SysEx 消息中的固件，或者一个并行端口。最终，有人会上传到 PCIe 上空的 Arduino 板上。