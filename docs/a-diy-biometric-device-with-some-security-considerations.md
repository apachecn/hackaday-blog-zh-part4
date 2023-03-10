# 有一些安全考虑的 DIY 生物识别设备

> 原文：<https://hackaday.com/2021/12/11/a-diy-biometric-device-with-some-security-considerations/>

生物黑客项目对黑客来说并不新鲜，它确实是一种真正激起我们兴趣的类型。我们最新的生物黑客设备是由[Manivannan]提供的，他带来了他的风格的可穿戴生物传感器，通过 AWS 内置了一些安全元素。

硬件由我们见过的一些令人印象深刻的组件组成。他有一个 [AD8232](https://hackaday.com/2021/05/03/ecg-project-with-all-the-messy-safety-details/) 心电图前端，有 [MAX30102](https://hackaday.com/2018/07/01/heartwatch-monitors-your-ticker/) 集成式脉搏血氧仪 IC 用于测定血氧和心率，有一直流行的 [LM35](https://hackaday.com/2021/02/19/practical-sensors-the-many-ways-we-measure-heat-electronically/) 用于测量体温。这两种芯片都非常适合你的下一个 DIY 生物传感器项目[，尽管你可能会尝试 MAX30205 体温传感器，因为它的精度为 0.1 摄氏度](https://hackaday.com/2017/07/22/hackaday-prize-entry-open-source-patient-monitor/)。然而，真正激起我们兴趣的是微芯片的 AVR-IoT WA 开发板的使用。[我们在](https://hackaday.com/2018/10/27/new-avr-iot-board-connects-to-google/)之前已经讨论过该板，也提到过您可能可以使用 ESP 设备做同样的事情，但现在我们可能会更多地看到该板的实际应用。

[Manivannan]向读者介绍电路板的设置，一切看起来都很简单。他最终组装了一个非常原始的仪表板，用于实时查看他的所有生命体征，演示了如何组装自己的患者仪表板，以远程监控生命体征或其他传感器信号。他强调，所有这些都是通过 AWS 实现的，这给他增加了一些安全层，这对保护他的数据免受不必要的查看者的访问至关重要。

虽然[Manivannan 的]安全实现没有达到医疗设备的标准，但它可能会成为日益发展的开源医疗设备运动中的一个案例研究。

 [https://www.youtube.com/embed/m2C7eXtU41U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/m2C7eXtU41U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

