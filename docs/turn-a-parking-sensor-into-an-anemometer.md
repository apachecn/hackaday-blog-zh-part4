# 将停车传感器变成风速计

> 原文：<https://hackaday.com/2021/10/28/turn-a-parking-sensor-into-an-anemometer/>

为了测量风速和风向，大多数人使用传统的风速计和风向标。另一种不太为人所知的方法是使用超声波换能器阵列，它不需要任何移动部件。[Andy]演示使用廉价的售后市场停车距离传感器套件和 Arduino 构建一个[超声波风速计。休息后的演示视频。](https://hackaday.io/project/181677-wind-sensor-using-car-reversing-kit)

除了价格之外，这些套件还具有额外的优势，包括防水超声波传感器，非常适合户外气象站，以及驱动它们所需的所有电路。需要进行一些电路手术来移除 Arduino Pro Micro 中现有的 8 引脚微控制器和导线，以及一些无源器件来控制脉冲输出和处理接收信号以计算方向和速度。超声波传感器安装在圆形底板上，指向安装在碳纤维棒上的“回波板”。[Andy]的最新版本还增加了一个 ESP8266 Wi-Fi 模块，用于连接。

DIY 环境传感器的挑战之一是校准它们以输出可靠的绝对值，尤其是风速。你需要另一个已知准确的风速计或已知速度的风源。不久前，我们报道了[【马建佳】的超声波风速计制造](https://hackaday.com/2021/07/06/open-source-ultrasonic-anemometer/)，他将它安装在他的汽车顶部，开始了他的驾驶，但仍然不能得到一致的结果。

虽然没有移动部件很好，但超声波风速计在软件和电子方面要复杂得多，DIY 杯型风速计仍然是一个可行的替代方案。

 [https://www.youtube.com/embed/_kloM0Tk8lo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_kloM0Tk8lo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

