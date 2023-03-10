# 你的家庭助理知道你什么时候睡觉吗？

> 原文：<https://hackaday.com/2019/09/11/does-your-home-assistant-know-when-you-are-sleeping/>

当我们意识到对人类孩子来说很简单的任务对计算机来说却是件大事时，总会给我们一种惊奇感。例如，如果你问某人你或其他人是否在睡觉，这是一件很简单的事情。对你来说，是的。对于计算机来说，它需要某种传感器。[Lewis]使用[称重传感器来判断某人是否在特定的床](https://everythingsmarthome.co.uk/howto/building-a-bed-occupancy-sensor-for-home-assistant/)上。他使用家庭助手，并有一个关于他如何创建和连接传感器的伟大帖子。当然，传感器只能告诉你床上是否有重物。它不知道它是谁，甚至不知道它不是一个塞满东西的手提箱。

称重传感器算不上什么高科技。有几种不同的类型使用液压或气动来测量力。然而，我们最常遇到的是使用应变仪。应变仪是一种电阻，当它变形时会改变值，称重传感器通常有几个应变仪以电桥配置连接，因此较小的力会产生较大的输出变化。

虽然桥式电路有利于提高灵敏度，但测量起来却是一个挑战。[Lewis]使用了一个分线板，该分线板配有一个 HX711 放大器和一个专为此目的制造的转换器。通过校准，称重传感器可以精确测量重量，但会有一些偏差。我们假设如果通常在你床上的人有非常不同的体重，你可能能够识别出谁在床上。

软件很简单，因为 HX711 有一个可用的 Arduino 库。最困难的部分可能是成功地为床腿制造一个脚轮来推动称重传感器。几年前，我们看到[一个浴室秤](https://hackaday.com/2017/09/21/load-cells-tell-you-to-lay-off-the-donuts/)以大致相同的方式建造。当然，重量并不是称重传感器测量的唯一力。例如，看看[【斯科比的】带锯](https://hackaday.com/2017/01/28/bandsaw-tension-gauge-uses-raspberry-pi-and-load-cell/)。