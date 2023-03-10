# 探测经过的 Starlink 卫星

> 原文：<https://hackaday.com/2021/11/29/detect-starlink-satellites-passing-by/>

Starlink 测试版已经半正式结束，但似乎全球芯片短缺仍在限制有多少卫星在世界各地飞行，为那些可能没有得到传统 ISP 服务的人提供宽带互联网接入。即使你可以注册，也不是世界上的每个地方都有覆盖，所以要检查这种状态很难，你可以[总是建立一个特殊的天线，当 Starlink 信标经过头顶时跟踪它们](https://sgcderek.github.io/posts/starlink-beacons/)。

[Derek]正在利用这个项目展示他的一些软件定义无线电技能，因此这将需要一个能够在 1600 MHz 范围内接收的 SDR。它还需要一个电源注入器来给卫星接收器供电，但这已经足够普遍了，因为它们是用来给电视天线供电的。来自 Starlink 卫星的信号具有非常高的信噪比，因此[Derek]甚至不需要一个碟形天线来聚焦信号。这也有帮助，因为他使用的天线能够看到更广阔的区域。一旦一切都设置好了，计算机正在监测光谱中的正确位置，他就能够非常清楚地看到卫星经过他身边的频率。

当然，[Derek]生活在一个信号覆盖非常好的地区，所以对于那些农村地区的人来说，这可能会有一点困难，但这可能不会持续很久，因为 Starlink 的目标是将宽带带给那些没有宽带的人。虽然这些卫星可能会在多大程度上干扰其他天文活动还存在一些问题，所以要持保留态度。

感谢[Spritle]的提示！