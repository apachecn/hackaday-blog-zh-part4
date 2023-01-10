# OpenDendrometer 可以测量你的树感觉如何

> 原文：<https://hackaday.com/2022/08/01/opendendrometer-can-measure-how-your-tree-feels/>

有各种方法来测量植物健康，我们已经看到许多项目创造开源解决方案。一个我们没有见过的是树木测量仪，它涉及测量树木的各种物理尺寸，以跟踪它们的健康和生长。[John Opsahl]正在用 open dendrometer 改变这种情况，这是一种追踪树枝和水果直径的工具。

直径的微小变化整天都在发生，跟踪这些变化可以检测到偏差，这可能是缺水的迹象。经过几个星期和几个月，这些测量可以用来测量生长和水果的收获进度。[John]发现数字轮胎胎面深度计可以很好地用于这种应用。许多这样的仪表使用与廉价的数字卡尺相同的电子设备，十多年前[串行协议被逆向工程](https://hackaday.com/2011/11/09/talking-digital-calipers-make-engineering-more-accessible/)得到。OpenDendrometer 通过 1.5V 电平转换器将轮胎深度计连接到微控制器，该转换器将测量结果记录到 SD 卡中，同时使用 DS3231 RTC 获得准确的时间戳。RTC 也可用于在所需的时间间隔唤醒电路，以节省电池电量。对于最初的概念验证，[John]使用的是 Arduino Pro Mini，但他计划在稍后阶段迁移到 ESP32，以支持无线数据传输。

所有东西都将被装在一个 3D 打印的外壳中，外壳上有一个泡沫衬垫，使设备能够抵御天气。外壳外部带有可调指旋螺钉的安装杆允许 OpenDendrometer 连接到树的任何部分。我们计划关注这个项目，并期待看到它产生的数据。

对于测量植物健康的其他方法，我们已经涵盖了从[土壤湿度](https://hackaday.com/2021/05/17/soil-moisture-sensors-how-do-they-work/)到[归一化差异植被指数](https://hackaday.com/2013/07/03/seeing-plant-health-in-infrared/)甚至植物重量甚至[盆栽植物重量](https://hackaday.com/2013/07/03/seeing-plant-health-in-infrared/)的所有内容。