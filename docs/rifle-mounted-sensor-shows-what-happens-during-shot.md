# 装在步枪上的传感器显示射击时发生了什么

> 原文：<https://hackaday.com/2019/01/23/rifle-mounted-sensor-shows-what-happens-during-shot/>

不熟悉射击运动的人有时意识不到让子弹去你想去的地方的物理性。在子弹沿枪管加速的短暂但有限的时间内，枪支最微小的移动都会产生弹道的巨大变化，目标越远，预计后坐力或猛扣扳机带来的潜在误差就越大。

像许多问题一样，这个问题更容易用你可以量化的东西来解决，这就是这个 DIY 步枪加速度计可以派上用场的地方。有一些商业单元设计用来做与[Eric Higgins]的设备相同的事情，但大多数价格都非常昂贵，因此 3 轴加速度计板售价 3 美元，滚动自己的设备是一项不错的投资。第 1 版使用 Arduino Uno 和加速度计板进行数据采集，使用 Raspberry Pi 进行分析，结果证明太笨重而不实用。下一个版本的足迹大大减少，羽毛和传感器安装在 3D 打印的托盘上，以便牢固地安装在步枪上。该传感器以大约 140 Hz 的频率捕捉数据，这足以显示射击时步枪上的任何意外移动。[Eric]能够使用数据找到至少一个他看起来退缩的例子。

我们喜欢像这样的真实世界数据记录应用，无论是从一辆自动越野汽车上抓取 ODB-II 数据还是记录足球发生了什么的 T2。我们将关注[Eric]对这个版本的改进计划，这会让它变得更加有用。