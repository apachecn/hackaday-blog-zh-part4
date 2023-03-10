# DIY 空气质量传感器

> 原文：<https://hackaday.com/2021/07/05/diy-air-quality-sensor/>

[Andrew Lamchenko]今年已经制造了许多基于电子墨水的小型传感器，他发布了另一个名为 [eON 室内空气质量传感器](https://hackaday.io/project/180248-eon-indoor-air-quality-sensor)的设计。正如他以前的传感器设计一样，eON 拥有一个引人注目的外观，与商业制造的产品完全一样。除了[Andrew]的设计是完全开源的。

除了显示空气质量，它还显示基本的天气状况，并且还有一个内置的天气预报算法。它可以独立运行，也可以使用无线电模块向智能家居系统发送读数。

![](img/ffec7cff15b5b11235209abf0d047906.png)

核心传感器是 SGP40，它可以检测空气中的挥发性有机化合物(VOCs)，同时功耗不到 3 mA(而上一代产品为 48 mA)。包装中还有温度、气压、湿度和光线传感器。像现在的许多项目一样，[Andrew]在这个过程中遇到了零件供应问题。因此，为了使设计更加灵活，我们设计了多种版本的评估板，以适应不同的排列组合:

*   显示
    *   2.13 英寸电子墨水显示屏
    *   DES 电子墨水显示器，即将推出
*   收音机，四种口味
    *   MINEW MS88SF3 (nRF52833、nRF52840)
    *   MINEW MS50SFA1 (nRF52810、nRF52811)
    *   MINEW MS50SFA2 (nRF52832)
    *   EBYTE E73-2G4M08S1C (nRF52833，nRF52840)
*   温度/压力传感器:
    *   BME280
    *   BMP280
    *   SHTC3

[Andrew]不仅设计了传感器，还在文档方面做了大量工作。查看该项目的 GitHub 知识库，获取涵盖设计所有方面的完整数据包，包括 John Young(恩智浦工程师，非宇航员)编写的天气预报应用笔记。上周[该设计被提名为 2021 年黑客日奖](https://hackaday.com/2021/06/28/ten-projects-won-the-rethink-displays-round-of-the-hackaday-prize/)的决赛作品。我们很期待看到从现在到 10 月底这段时间他会怎么做！

你在家里使用空气质量传感器吗？如果是这样的话，它只是为了提供信息还是你根据数据采取行动，比如自动打开风扇或者逃到乡下？请在下面的评论中告诉我们。

The [HackadayPrize2021](https://prize.supplyframe.com) is Sponsored by:[![Digi-Key](img/e7d13a315fd6226594212ca8f8762832.png)](https://www.digikey.com/)[![Supplyframe](img/fdb8a432506edeeafacfef227b3d3b33.png)](https://supplyframe.com/)