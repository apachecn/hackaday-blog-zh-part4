# 带有 ESP32 的便携式家用空气质量测量仪

> 原文：<https://hackaday.com/2020/07/20/a-portable-home-air-quality-meter-with-the-esp32/>

在世界各地，疫情的轮流封锁让许多人在家工作。[kn100]就是这样一个困境，当他一天 24 小时都呆在一个住宅公寓里时，他开始对空气质量感到疑惑。因此，是时候制造一些装置来监视事物了！

![](img/0de9e1f034177468184b2895adecff3b.png)

Grafana may require a database and some work to set up, but the results are to die for.

该建筑包括一个连接到博世 BME680 空气质量传感器的 ESP32。它测量压力、温度、湿度和气体阻力，然后通过一个封闭的源代码库，使用这些数据来计算“空气质量指数”，并估计空气中的 CO2 和 VOC 水平。数据通过 MQTT 从 ESP32 传递到 Raspberry Pi。这会运行 Mosquitto 来处理 MQTT 查询，将数据保存在 Influxdb 实例中。然后使用 Grafana 查询这个数据库，并生成数据的吸引人的图表。

这种构建不仅有助于监视公寓中的事物，而且是构建具有顶级数据可视化的可靠物联网设备的伟大实践。[我们之前也讨论过如何做到这一点](https://hackaday.com/2019/01/23/howto-docker-databases-and-dashboards-to-deal-with-your-data/)——所以如果你在生活中需要这种能力，就没有理由不被黑客攻击！