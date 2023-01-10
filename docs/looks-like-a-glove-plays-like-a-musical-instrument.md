# 看起来像手套，演奏起来像乐器

> 原文：<https://hackaday.com/2018/10/25/looks-like-a-glove-plays-like-a-musical-instrument/>

GePS 是一个音乐项目，展示了手势控制的集成工作是多么重要。创作者[Cedric Spindler]和[Frederic Robinson]演示了如何使用手持 IMU(惯性测量单元)和磁力计的输出将动作、手势和快速抓拍运动转化为音乐输出。GePS 被设计成具有足够的可重复性和足够低的延迟，使得反馈几乎是即时的。因此，它可以像任何其他乐器一样使用和演奏，以可预测的方式从物理运动中产生声音。在这方面，它与[特雷门琴](https://hackaday.com/2016/01/24/finally-a-modern-theremin/)没有什么不同，但更易于配置。

为了做到这一点，[Cedric]和[Frederic]用 CurieNano 板(基于[英特尔的 Curie](https://hackaday.com/2015/10/16/intel-and-arduino-introduce-curie-based-educational-board/)，它也有 IMU 板载)和 XBee 无线电制作了 GEP，用于无线连接到计算机上运行的软件，从那里播放声音。该设备的灵敏度和低延迟意味着即使是很小的动作也可以被可靠地捕捉到，这意味着手每天所做的那种流畅而复杂的动作可以作为播放声音和即时反馈的基础。在非常真实的意义上，基于手套的 GePS 是一种实验性的新乐器，这使它成为 2018 年 Hackaday 奖[乐器挑战赛](https://hackaday.io/prize/details#five)部分的一个迷人竞争者。

The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)