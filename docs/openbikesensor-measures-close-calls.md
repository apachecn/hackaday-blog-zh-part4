# OpenBikeSensor 测量近距离呼叫

> 原文：<https://hackaday.com/2022/02/05/openbikesensor-measures-close-calls/>

骑自行车有趣、健康，并且对环境有益。但不幸的是，这并不总是最安全的活动，因为不体贴的司机对骑自行车的人来说是一个重大的危险。包括德国、法国和比利时在内的几个国家已经立法要求汽车和自行车之间的最小超车距离至少为 1.5 米。然而，执行这样的规则是很棘手的，没有准确的平均超车距离数据，很难知道有多少司机在遵守这条规则。

进入 [OpenBikeSensor，这是一个开源硬件和社区科学项目](https://www.openbikesensor.org/en/)，旨在准确收集这些信息。目前处于原型阶段，它的目标是制造一个简单的自行车安装传感器，测量与任何过往车辆的横向距离。由此产生的数据被在线收集，以生成突出危险区域的地图，最终可被城市规划者用于改善自行车基础设施。

硬件基于一组超声波传感器，可以测量到任何大型物体的横向距离。GPS 模块跟踪自行车的位置，而 ESP32 读取数据并将其存储在 SD 卡上。用户界面由安装在车把上的显示器组成，显示系统的状态。还有一个按钮，用户需要在车辆经过时随时按下:这将触发测量并记录位置。回家后，用户可以将 OpenBikeSensor 连接到他们的 WiFi 网络，并下载他们的行程数据。

最初的结果看起来很有希望，任何让人们同时骑自行车和摆弄电子产品的项目都值得研究。这也不是我们第一次看到自行车上安装的传感器:人们已经设计了自己的传感器来测量南美洲的空气污染，或者简单地测量 T2 自己自行车的速度，或者 T4 的轮胎压力。

 [https://www.youtube.com/embed/YrpipBDGe9s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/YrpipBDGe9s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

