# E-Ink 装备酸面团发酵剂罐

> 原文：<https://hackaday.com/2021/07/03/e-ink-equipped-sourdough-starter-jar/>

我们的这种疫情的一个意想不到的副作用是全球被捕获的乳杆菌和酵母菌落的突然增长。也被称为酸面团发酵剂，它们通常装在罐子里，上面写着奇怪的名字，靠面粉和水的混合物为生。它们需要密切监控以保持健康，并确定何时可以烘烤。在过去的两年里，诺亚·费恩一直致力于将这一过程仪器化和自动化，并创造了一个高科技罐子来监视他的酸面团发酵剂。

为了让发酵剂保持活性，它必须保持在一定的温度范围内，而性能是通过罐子内的液位上升多少来衡量的。现有的[开源](https://hackaday.com/2021/03/04/smart-lid-spies-on-sourdough-starter-sends-data-wirelessly/)和[商业](https://breadwinner.life/buy)项目监控这两个参数并传输数据出去，但是【诺亚】想要包含更多的特性。由于二氧化碳的产生，酸面团发酵剂的高度会上升，因此他增加了一个 SCD-30 传感器模块，其中包括一个温度和湿度传感器。对于液位监控，VL6180 飞行时间传感器安装在罐子顶部的一个孔上。[Noah]希望能够在罐子上看到最近的二氧化碳产量和高度统计数据，使用了带有板载电子墨水显示器的 ESP32 模块。为了以恒定的速率将空气吸入 CO2 传感器，还添加了一个小型抽风机。电力由一个小型脂肪电池提供。对于长期记录，数据通过 MQTT 发送到运行[mycode](https://hackaday.com/2016/09/14/hackaday-prize-entry-environmental-regulation/)环境管理软件的服务器。

[Noah]仍然希望对软件进行一些改进，包括电池寿命、用户界面和提醒，但所有东西都是开源的，可以在 GitHub 上获得，所以可以自由地加入并构建自己的软件。