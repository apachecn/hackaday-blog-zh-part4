# 您的 PC 声卡作为传感器输入

> 原文：<https://hackaday.com/2021/07/03/your-pc-sound-card-as-a-sensor-input/>

商品化的个人电脑是我们许多人将拥有的最通用的工具，由于它已经存在了很长时间，如果最新的组件不是一个问题，它也可以免费或非常便宜地找到。虽然它不是没有限制，但它是为扩展而设计的，它不再有任何端口可以轻松地重新用作读取传感器的 GPIOs。[Ruslan Nagimov][为我们展示了 PC 声卡如何成为测量接口](https://nagimov.me/post/measure-with-music-how-to-read-analog-sensors-using-a-pc-sound-card/)，为我们提供了一些传感器的解决方案。

其思想是，简单的电阻或电容传感器可以通过其交流特性读取，方法是在卡的一个通道上发送正弦波，在另一个通道上从分压器电路读取结果。他深入研究了代码，包括电阻示例和电抗组件，我们可以看到，这是对 PC 功能的方便扩展。

我们确信这项技术会为一些读者找到应用，但它让我们对另一个平台感兴趣。[使用手机音频插孔进行测量并没有令人振奋的历史](https://hackaday.com/2016/11/17/instrument-apps-on-your-phone-the-christmas-cracker-novelties-of-the-test-bench/)，但这或许也可以用于移动传感器。