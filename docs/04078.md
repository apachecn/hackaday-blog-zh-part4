# 建立一个全脂肪空气质量监测器

> 原文：<https://hackaday.com/2019/09/03/building-a-full-fat-air-quality-monitor/>

多年来，许多人建立了一个空气质量监测站，通常是一些测量颗粒物(PM [2.5] & PM [10] )的配置。有些还会测量臭氧(T4)，但很少会达到美国环保署和其他组织计算空气质量指数(AQI)的要求。[【Ryan Kinnett】的项目](https://hackaday.io/project/167435-a-more-complete-air-quality-monitor)就是那些有 AQI 能力的站之一。

[AQI](https://en.wikipedia.org/wiki/Air_quality_index) 需要测量前述 PM [2.5] (克/米 ³ )、PM [10] (克/米 ³ )和 O [3] (ppb)，还需要测量 CO (ppm)，因此 [2] (ppb)和 NO [2] (ppb)，所有这些都必须以特定的灵敏度和容差来完成。这意味着获得足够灵敏的传感器，并进行校准。[Ryan]找到了一家名为[Spec Sensors](https://www.spec-sensors.com)的公司，他们销售的传感器非常适合这个目标。

使用 Spec Sensor 针对臭氧、二氧化氮、一氧化碳和二氧化硫的超低功耗传感器模块(ULPSM ),针对空气温度、压力和相对湿度的 BME280，以及 Plantower PMS5003 激光粒子计数器和 ADS1115 ADC，创建了一个与基于 ESP8266 的 NodeMCU 板完美配合的封装，为读取这些传感器提供了一种便捷的方式。一次性 BOM 总成本约为 250 美元。

可以读出结果数据，并从中计算出 AQI，从而得到所需的结果。最初[Ryan]计划带着这个传感器包在洛杉矶兜一圈，以获得比环保局目前提供的更多的空气质量指数数据，但传感器稳定和平均读数需要时间(1 小时)，这将需要很长时间才能获得大面积的读数。

理想情况下，许多这样的节点应该安装在该地区，但这将相当昂贵，这给[Ryan]提出了一个问题，即如何才能将它提高到洛杉矶地区的空气质量公民科学项目的水平。请在评论中留下你的想法和建议。