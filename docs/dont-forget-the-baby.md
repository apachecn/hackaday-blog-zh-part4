# 别忘了宝宝！

> 原文：<https://hackaday.com/2019/12/05/dont-forget-the-baby/>

这一定是父母们普遍的担心，他们可能会忘记他们的孩子，把他们留在车里，因为那里太热了。以至于[Matt Meerian]制作了一个闹钟，当汽车关闭时，它会发出口头提醒来检查这个年轻人。

这是一个足够简单的设备，有一个 ATmega328，一个现成的 MP3 模块和一个电源调节器，可以从车辆附件插座的 12 V 向一对超级电容器提供 5 V 电压。这个想法是当车辆点火关闭时，电源会被切断，超级电容器内部有足够的能量播放提醒样本，供司机检查是否有被遗忘的儿童。

我们不禁注意到，一定比例的汽车会一直开着附件插座，因此思考一下在这种情况下如何检测到汽车被关闭将会很有趣。他考虑用一部多余的手机代替他的 ATmega328，也许手机上的 MEMS 传感器也可以用来检测发动机关闭时停止的振动。尽管有这样的车，这个装置是解决手头问题的直接方法。

The [HackadayPrize2019](https://prize.supplyframe.com) is Sponsored by: [![Supplyframe](img/79a7db035b8a2b6c2b7b0895c45b7de8.png)](https://supplyframe.com/)  [![Digi-Key](img/ba094a14c430ab81591a2abdc54a5363.png)](https://hackaday.io/digikey)  [![Microchip](img/5023ef0b7ff1aee311cba9b54a3ac9fe.png)](https://hackaday.io/microchip)