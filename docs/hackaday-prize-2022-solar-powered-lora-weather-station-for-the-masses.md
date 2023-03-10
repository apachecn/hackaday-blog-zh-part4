# 2022 年 Hackaday 奖:面向大众的太阳能劳拉气象站

> 原文：<https://hackaday.com/2022/09/22/hackaday-prize-2022-solar-powered-lora-weather-station-for-the-masses/>

【Debasish Dutta】过去设计过几个气象站，而这个 [系统的第四个版本](https://hackaday.io/project/187061-solar-powered-wifi-weather-station-v40) 已经收到了过去用户的许多功能请求。该站旨在与 Sparkfun 提供的外部天气传感器单元一起使用。这处理风速和风向，以及测量降雨量。一个定制 PCB 承载一个 ESP32-WROOM 模块和一个 Ai-Thinker Ra-02 LoRa 模块，分别用于控制和连接。PMS5003 位于 PCB 上，用于测量这些颗粒密度，但大多数传感器都通过简单的 4 路 I2C 连接器连接。温度、湿度和压力由 BME280 模块处理，紫外线指数(SI1145)、可见光(BH1750)甚至土壤湿度和温度由电缆安装的 SHT10 模块处理。

所有这些都由太阳能电池板供电，它为 18650 电池充电，并在黑暗的时间里保持节目的运行。对于调试和部署，USB-C 电源端口也可用于充电。[一个 3D 打印的 Stevenson screen](https://hackaday.com/2022/02/04/3d-printed-radiation-shields-get-put-to-the-test/) 型外壳允许空气在 PCB 安装的传感器模块之间流通，希望不会有太多的水分进入其中造成损害。

在数据收集和可视化方面，一个配套的 LoRa 接收器模块正在开发中，该模块旨在将测量结果传递给各种服务。想想家务助理，尤其是家务助理之类的。软件仍然是一项进行中的工作，所以也许以后再回来看看[Debasish]是如何进行的？

这种多传感器托管项目在这里已经不是什么新鲜事了，这里有一个 [2019 Hackaday prize 参赛作品与此一脉相承](https://hackaday.com/2019/05/03/low-power-weather-station-blows-the-competition-away/) 。当然，收集和记录测量数据只是问题的一部分，这些测量的可视化也很重要。为什么不用一个 [的机械方法，比如一个](https://hackaday.com/2022/03/12/build-yourself-a-weather-reporting-diorama/) ？

The [HackadayPrize2022](https://prize.supplyframe.com) is Sponsored by:[![Digi-Key](img/e7d13a315fd6226594212ca8f8762832.png)](https://www.digikey.com/)[![Supplyframe](img/fdb8a432506edeeafacfef227b3d3b33.png)](https://supplyframe.com/)