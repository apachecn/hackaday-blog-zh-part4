# 一枚四年前的活动徽章成为了环境传感器

> 原文：<https://hackaday.com/2021/02/04/a-four-year-old-event-badge-makes-an-environmental-sensor/>

到现在为止，我们都已经习惯了疫情提出的社交距离和在室内戴口罩的要求。但正如[poly loyd]和荷兰阿默斯福特 Bitlair hackerspace 董事会的其他成员所担心的那样，在建筑物内仍有风险因素需要考虑。没有新鲜空气，病毒携带液滴的浓度会增加，他们能想到的最好的监测方法是安装一套二氧化碳传感器。为了运行它们，他们不需要购买任何新的硬件，[而是求助于一套来自 2017s SHA 黑客营](https://polyfloyd.net/post/co2-sensors-against-covid/)的活动徽章。

这个徽章展示了一个带有电子墨水屏幕的 ESP32 模块，对于这个项目来说，最有趣的是它仍然有一个受支持的软件平台和一个方便的后部扩展连接器。常见的 MH-Z19 红外 CO2 传感器和 BME280 湿度传感器安装在一个 PCB 上，该 PCB 遵循徽章的形状，顶部有一个突起，在其上它们看起来像一个集成单元。处理这些读数的是一个 MicroPython badge 应用程序，它通过 MQTT 发出警告，并在屏幕上绘制二氧化碳图表。一切都是可用的，既有[GitHub 库中的硬件](https://github.com/polyfloyd/sha2017-badge-co2-sensor)，也有[作为 badge.team 应用的软件](https://badge.team/projects/sha2017_badge_co2_sensor)。

我们赞扬任何在项目中使用活动徽章的人，尤其是在活动结束一年后使用徽章的人。SHA 徽章及其后代通过其良好支持的平台独一无二地适合于此，因此如果您在抽屉中有一个徽章，我们强烈建议您拿出来试一试。