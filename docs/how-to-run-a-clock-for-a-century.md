# 如何运行一个世纪的时钟

> 原文：<https://hackaday.com/2018/08/05/how-to-run-a-clock-for-a-century/>

无人看管的情况下，什么能让一个钟持续运转一个世纪？好吧，不管它在运行什么，它都需要消耗能量，而且它需要一个能持续很长时间的电源。[Jan Waclawek]正在研究白天用太阳能，晚上用电容器，以保证他的[钟为](https://hackaday.io/project/159663-clock-for-a-century) [运行一百年](https://hackaday.io/project/159663-clock-for-a-century)。

这个项目延续了[Jan]之前的项目,研究什么样的电源可以在不需要干预的情况下为他家周围的设备供电一个世纪——即无需更换电池，无需缠绕等。[Jan]他选择了太阳能和聚丙烯薄膜电容器的组合。一旦对电源进行了分类，就选择一个时钟来测试电源。时钟的功耗在夜间会很低——它只需要一个 RTC 电路来记录时间——因此可以使用一些低泄漏电容。当日光返回或灯打开时，太阳能电路将为时钟的显示供电。

目前，[Jan]有一个概念验证电路正在工作，使用 STM32L476 发现板上的超低功耗微控制器和几个 10 μF 0805 大小的电容器，当太阳能电池板充满电时，时钟的显示持续大约两分钟。

查看[Jan]的项目以了解更多细节，并查看他之前的项目，在该项目中，他缩小了百年电源的组件范围。休息之后，可以看到[Jan]的原型。再看看这个[主时钟，它给从时钟](https://hackaday.com/2017/03/29/power-sipping-master-keeps-slave-clock-on-time/)发信号，用一节 AA 电池运行一年。

The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/) 

 [https://www.youtube.com/embed/4WnCrePNtlc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/4WnCrePNtlc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

