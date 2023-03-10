# 监控你上下班路上的污染

> 原文：<https://hackaday.com/2019/06/22/monitor-the-pollution-on-your-commute/>

在 21 世纪的城市中，通勤会带来大量的污染。对于 Medway Makers 成员来说，这意味着伦敦的狗岛，以及穿过泰晤士河下的黑墙隧道。当你能尝到空气中的污染时，很明显这不是最好的环境，但是到底有多糟糕呢？是时候组装一个环境监测和记录设备了。

内置了一个 ESP32 模块，一个 SPS30 颗粒传感器，一个 MH-Z19 CO₂传感器，一个 HTU21D 温度和湿度传感器，以及一个 uBlox NEO 6M GPS 模块。最终的计划是添加一个用于数据记录的 SD 卡，但在没有 sd 卡的情况下，它会连接到一个通过 [InfluxDB](https://www.influxdata.com/) 运行 [Grafana](https://grafana.com/) 的 Raspberry Pi 来进行数据分析。这一结果不仅为通勤环境质量，也为室内生活环境质量提供了一个令人惊讶的视角。我们很抱歉地说，他们似乎没有在 Medway Makers 的文章中发布任何相关的代码，尽管我们希望这是一个疏忽，他们会在此上线时纠正。

这并不是第一份为这些页面增色的环境监测报告，事实上[我们已经有了不少 Hackaday 奖的参赛作品](https://hackaday.com/2015/04/22/earth-day-environmental-sensors/)。