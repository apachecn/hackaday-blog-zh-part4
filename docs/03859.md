# 健身追踪器不一定是专有的

> 原文：<https://hackaday.com/2019/08/11/fitness-trackers-dont-have-to-be-proprietary/>

健身追踪器已经成为一种流行的消费电子设备，各种制造商生产了一系列型号。然而，这些商业产品中的许多给消费者留下了他们的数据被提取到云服务器并出售给出价最高者的前景，以牺牲隐私为代价换取了便利。如果有一个健身追踪器提供完全控制！

[open hak 是一款开源健身追踪器](https://hackaday.io/project/167036-openhak),装在一个 3D 打印的手表外壳中，可以测量你的心率并计算你的步数，通过蓝牙为你提供收集的结果数据。它的核心是一个 Sparkfun Simblee 模块，通过 Maxim MAX30101 和计步来感知心率。被一个 Bocsh BMI160。它从一开始就为可扩展性而设计，带有一个引出有用的接口线的标题。在原型中，他们用这个来支撑一个小型的有机发光二极管显示器。其结果是，一款健身追踪器手表可能无法与一些知名的专有设备相媲美，但它仍然完全开放，而且价格可能也低得多。

这些年来，我们已经看到了相当多的健身追踪器应用，包括[转换成脑电图](https://hackaday.com/2018/08/30/turning-a-fitness-tracker-into-an-eeg/)，以及[为一些商业追踪器定制的固件](https://hackaday.com/2019/02/20/custom-firmware-for-cheap-fitness-trackers/)。