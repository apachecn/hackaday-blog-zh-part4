# 发现这个 DIY 电子负载的优雅隐藏的黑客

> 原文：<https://hackaday.com/2019/02/28/spot-this-diy-electronic-loads-gracefully-hidden-hacks/>

有时需要用手头上的任何零件来凑合，但将一个方形钉挤压成一个圆孔的结果并不总是像[Juan Gg]的[可编程 DC 加载旋转编码器](https://juangg-projects.blogspot.com/2019/02/arduino-based-electronic-load.html)那样优雅。[Juan]采用了一种可编程 DC 负载的设计，并以多种不同的方式将它变成了自己的设计，包括一个光滑的 3D 打印外壳和彩色面板。

首先吸引人眼球的可能是最左边的七段数字。有一个简单的原因，它不匹配它的邻居:[胡安]不得不使用他可用的，这意味着一个不匹配的数字。幸运的是，3D 打印自己的外壳意味着它可以优雅地融入设计中，而不是使用 Dremel 或美工刀。下一个不太明显:显示屏的第二位缺少小数点，所以下面塞了一个 LED 来完成这项工作。最后，右边的旋钮可以合理地认为是一个旋转编码器，但它实际上是连接到一个小 DC 电机。通过在一根导线上施加一个小的 DC 电压来偏置电机，并从另一根导线上读取产生的电压，可以检测旋钮的速度和方向，作为旋转编码器的替代品来完成一项可维护的工作。

该项目的 [GitHub 库](https://github.com/JuanGranja/Arduino-Based-Electronic-Load)包含了【Juan】项目的 Arduino 代码，其根源在于[一个详细描述电子负载](https://hackaday.com/2010/08/06/dummy-loads-and-heat-sinks/)的设计 EEVblog。对于那些喜欢 DIY 旋转编码器发送离散点击和脉冲而不是模拟电压的人来说，[一个 3D 打印轮和两个微型开关](https://hackaday.com/2018/02/19/roll-your-own-rotary-encoders/)将完成这项工作。