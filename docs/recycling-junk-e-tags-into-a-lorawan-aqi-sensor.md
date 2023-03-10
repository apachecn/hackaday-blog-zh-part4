# 将垃圾电子标签回收到 LoRaWAN AQI 传感器中

> 原文：<https://hackaday.com/2022/09/28/recycling-junk-e-tags-into-a-lorawan-aqi-sensor/>

![E-paper interfacing circuit is just a simple switched-mode power supply](img/9781d917c1b7ce18c373b87532501f95.png)

Interfacing to E-paper displays is nothing to be scared of

[adu echo]看到了那些基于电子纸的价格标签的廉价易贝交易，并想知道它们是否可以被黑客攻击来执行一些其他任务。拆开外壳后，发现控制器芯片是一个 SEM9110，有一些 NFC 硬件支持，但其他几乎没有。[aduecho]希望建立一些 [物联网空气质量指标(AQI)单元](https://hackaday.io/project/187272-lorawan-aqi-sensor-with-e-paper-display) 但是缺乏 SEM9110 的数据表，加上没有传感器，这意味着唯一真正的行动是丢弃 PCB，只保留电子纸显示器和电池。这些单位似乎是“新老”股票，所以很有可能都是新鲜和成熟的采摘。

PCB【adu echo】拿出来的在机械上和原来的单元是一样的，但是现在运动了一个 Seeed studio[Wio-E5 LoRa 模块](https://wiki.seeedstudio.com/LoRa-E5_STM32WLE5JC_Module/) ，它使用 ST 的 STM32WLE5 进行重载。这看起来像一个 Semtech SX126x 集成在芯片上(我们想不出一种合理的方式来倒装一个实际的 SX126x 芯片，但你永远不会知道)。使用这个模块是轻而易举的，只需要非常少的天线匹配元件和一点去耦就可以工作。在感测方面，一个 [博世 BME680 气体传感器](https://www.bosch-sensortec.com/products/environmental-sensors/gas-sensors/bme680/) 处理 AQI 测量，一个 [博世 BMI270 6 轴 IMU](https://www.bosch-sensortec.com/products/motion-sensors/imus/bmi270/) ，提供陀螺仪和加速度计，用于所有那些计划的用户交互功能。从 [原理图](https://cdn.hackaday.io/files/1872728012245248/EPD_2P9_Lora_AQI.pdf) 中可以看出，EPD 的接口非常简单，只需要少量器件就可以通过简单的 SMPS 电路产生必要的双极性栅极电压。显示控制器通过 SPI 接口编程，在内部进行处理。

在这个项目中，我们非常喜欢的一个方面是整洁的手绘图标和可变宽度的字体，当在低对比度的电子纸显示器上绘制时，给显示器一种笔记般的质量。

空气质量测量项目不时地点缀这些页面，就像这个 [黑掉的宜家 Vindriktning](https://hackaday.com/2021/08/13/hacked-ikea-air-quality-sensor-gets-custom-pcb/) ，还有这个非常相似的 [基于 Wio-E5 的项目](https://hackaday.com/2022/08/30/lora-air-quality-monitor-raises-the-bar-on-diy-iot/) 我们上个月报道过。