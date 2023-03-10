# 本周失败:雄心勃勃的矢量网络分析仪未能交付

> 原文：<https://hackaday.com/2019/12/31/fail-of-the-week-ambitious-vector-network-analyzer-fails-to-deliver/>

如果你要失败，你最好雄心勃勃地失败。一个包含许多子系统的复杂项目有更大的机会至少取得部分成功，同时也提供了宝贵的经验，告诉我们下次不要做什么。至少，这是[乔希·约翰逊]用低成本矢量网络分析仪的柠檬制成的柠檬水。

对于外行来说，VNA 是 RF 工作的多功能测试仪器，允许您测量信号的幅度和相位，它可以用于从天线和滤波器设计到表征传输线路的一切。[Josh]决定将他的低成本 VNA 的许多功能移植到主机上，并专注于设计的各个 RF 阶段。不幸的是，[Josh]发现完成的 VNA 的性能有所欠缺，尤其是在相位测量部分。他在论文中对故障模式进行了完整的分析，但简短的内容是对来自本地振荡器的谐波滤波不佳、位于其设计核心的 AD8302 芯片的意外行为以及校准问题。混淆这些问题的是时间限制；[Josh]如果学年没有结束的话，问题可能已经解决了。

在通读了[Josh]对他的项目的描述后，我们觉得他对构建失败的评价有点苛刻，这是一个最后一年的项目，也是他论文的一部分。也许雄心勃勃，但是随着大量低成本的 vna 上市，我们可以看到他从哪里得到的灵感。我们理解[Josh]的失望，但是从优秀的构建质量到一流的文档，这里有很多成功之处。