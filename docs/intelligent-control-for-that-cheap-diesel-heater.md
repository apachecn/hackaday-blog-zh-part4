# 廉价柴油机加热器智能控制

> 原文：<https://hackaday.com/2019/09/21/intelligent-control-for-that-cheap-diesel-heater/>

如果你有一辆房车或一艘船，你会知道保持温暖是一件很困难的事情。明火气体加热器有一氧化碳中毒的风险，而固体燃料炉很重，需要安全烟道。柴油加热器的前景是诱人的，因为它们使用更安全的燃料，并允许轻松的外部排气。不幸的是，它们一直是一种昂贵的选择，但近年来廉价进口加热器的出现使它们成为一种有吸引力的选择。[雷·琼斯]已经通过[加力燃烧室、](http://www.mrjones.id.au/afterburner/)改进了他们有时基本的控制电子设备，这是一种智能控制器，它封装了 ESP32 和 HC-05 模块，以增强设备的功能集和连接性。

完整的功能列表有些详尽，但有一些突出的功能，如将 1 线温度传感器连接到系统的能力。它并不与市场上所有的加热器兼容，但有一个全面的指南可以指导这些型号的加热器。同时，所有代码和其他资源都可以在 [GitLab](https://gitlab.com/mrjones.id.au/bluetoothheater) 上找到，如果你想自己尝试的话。

柴油在 2019 年是一个肮脏的词，但也许[生物柴油](https://hackaday.com/2013/08/03/biodiesel-equipment-hacks/)将拯救像这样的设备。

谢谢[鲍勃]的提示！