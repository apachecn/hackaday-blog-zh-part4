# 智能卫生纸架记录白金

> 原文：<https://hackaday.com/2020/06/26/smart-toilet-paper-holder-keeps-track-of-white-gold/>

当我们在 2020 年的元旦醒来时，很少有人会预测到在短短的几个月内一切会变得多么糟糕。全球卫生纸短缺只是冰山一角，这让每个人都更加关注自己家里的库存。这是[thepenguinmaster]决定尝试在云中管理的事情。[进入智能卫生纸卷筒。](https://www.element14.com/community/groups/azuresphere/blog/2020/06/10/smart-toilet-paper-roll)

该设备由一个 3D 打印的卫生纸架组成，配备有传感器来跟踪这种珍贵材料的使用情况。磁性旋转编码器用于监控卷的旋转，激光雷达设备用于感应用户的手何时靠近。数据通过 Avnet Azure Sphere MT3620 传输到云端。与 Azure 的链接允许自动生成图表并通过互联网从任何地方访问。

该项目表明，房子周围的任何东西都可以通过互联网进行监控。我们希望看到跟踪器走得更远，以每张纸为基础测量使用情况，并在供应不足时自动订购更多。我们以前也见过类似的工作。