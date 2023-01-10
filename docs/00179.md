# 高效率，开源 MPPT 太阳能充电器

> 原文：<https://hackaday.com/2018/07/31/high-efficiency-open-sourced-mppt-solar-charger/>

几年前，[Lukas fs sler]需要一个太阳能充电控制器，于是他自己做了一个，并一直在改进。设计现已成熟，[高效 MPPT 太阳能充电器](https://hackaday.io/project/158859)拥有数据记录等全部功能，在 1 到 75 瓦的范围内拥有 97%的效率，可以作为独立单元使用，也可以作为模块集成到其他系统中。在这个过程中，[Lukas]清楚的一件事是，一个高效、功能丰富、开源的充电控制器硬件解决方案根本不存在，至少不具备他心目中的功能。

数据记录和高效率对于充电控制器来说非常重要，因为电池在充电时会有不同的特性，太阳能电池板等设备产生的电能也会在不同的条件和负载下发生变化。MPPT(最大点功率跟踪)充电器是一个智能单元，优化处理所有这些变化的条件，以实现最高效率。[我们过去曾详细介绍过 MPPT](https://hackaday.com/2017/03/17/are-you-down-with-mppt-yeah-you-know-me/) ，经过三年的开发，创造了一个模块化和可配置的设计，[Lukas]希望没有人需要重新发明充电控制器。

The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)