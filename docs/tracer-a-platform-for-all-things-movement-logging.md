# Tracer，一个所有事物运动记录的平台

> 原文：<https://hackaday.com/2022/04/01/tracer-a-platform-for-all-things-movement-logging/>

【elektroThing】正在[建造一个轻量级的电池供电板](https://hackaday.io/project/184499-tracer-a-wearable-for-things)来跟踪和测量各种运动，称为 Tracer。由 ESP32 供电，它有一个 LSM6DSL 6DoF 加速度计&陀螺仪传感器和一个 VL53L0X 飞行时间传感器。据报道，支架中的一个小型锂离子电池可以通过蓝牙低能量(BLE)以 100 赫兹的频率提供 5 小时的流媒体数据。它本质上是一个无线运动传感器平台，与一台更强大的计算机配对，用于数据记录和分析。这样的平台有什么用？

他们展示了附在网球拍上的数据，说你可以用这些数据来计算一场比赛中的击球次数。他们还把它绑在自行车的曲轴上，并把它作为一个节奏传感器——很好地测量你的骑行效率！但是当然，这可以用在比运动更多的应用中。像这样的设备可以用来记录任何相对靠近的物体的运动，无论是你的猫，办公椅，还是某人有时用力过猛的门。比方说，你想开发一个睡眠追踪器，并收集一些数据来定义你的算法和规划你的硬件需求——这将创造奇迹。

已经有可用的[示例代码](https://github.com/elektroThing/Tracer/tree/main/software/Tracer)用于将数据流式传输到 [Phyphox 数据记录和绘图应用](https://phyphox.org/)，以及[原理图](https://github.com/elektroThing/Tracer/blob/main/schematic.pdf)——希望完整的电路板文件将很快可用。这个平台是用于类似目的的商业设备的一个有价值的开源对手，对于任何想做运动测量项目而又不想立刻重新发明几个轮子的黑客来说都是一个好消息。我们被告知这款主板可能很快就会上市，我们已经等不及了！像这样的平台，如果做得好，可以产生新项目的后代，让我们从中获得乐趣，并且我们的付费项目[在](https://hackaday.com/2016/06/09/data-logging-everyones-doing-it-why-arent-you/)上工作会容易得多。

我们以前展示过带有这种传感器的项目——这里有一个[通过给你数据来调试你最后一秒钟的步枪运动来帮助你的步枪瞄准](https://hackaday.com/2019/01/23/rifle-mounted-sensor-shows-what-happens-during-shot/),另一个[记录足球](https://hackaday.com/2011/01/09/data-logging-football/)内部的运动数据。你可以将数据传输到一百万个终端，我们被告知[你甚至可以使用谷歌表单。](https://hackaday.com/2012/05/31/data-logging-directly-to-google-docs-google-drive/)就在一年前，我们[举办了我们的数据记录比赛](https://hackaday.com/2021/03/02/new-contest-data-loggin/)和[我们收到的参赛作品](https://hackaday.com/2021/05/01/winners-of-hackadays-data-loggin-contest-bluetooth-gardening-counting-cups-and-predicting-rainfall/)一定会指出你日常生活中相当多的未开发领域！