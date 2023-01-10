# 用树莓皮探索地下室湿度

> 原文：<https://hackaday.com/2019/07/01/exploring-basement-humidity-with-a-raspberry-pi/>

有时候，黑客并不是要构建一些很酷的东西。有时它更具战术性，将正确的材料拼凑在一起以收集决策所需的信息，或者只是记录一些有趣的现象。

就拿【马蒂亚斯·万德尔】进行的这个即兴但彻底的地下室湿度探索来说吧。像大多数家里有成品地下室的人一样，[马提亚斯]觉得湿度大得令人讨厌，需要搬走。但他不是那种把除湿机扔在那里就忘了的人。为了寻找设备工作情况的数据，[Matthias]将 DHT22 温度/湿度传感器连接到备用的 Raspberry Pi 上，以监控房间条件，并将除湿器插入 Kill-A-Watt，Pi 摄像头对准显示器，以捕捉用电数据。

他的结果很有趣。这种设备确实降低了房间的湿度，同时提高了温度，考虑到除湿机的工作方式，这并不是一个意料之外的结果。但是在湿度上有一个奇怪的周期性峰值，对应于电器的定期除霜循环将湿气驱回房间。当除湿机关闭时，房间湿度逐渐增加，这表明水的来源不明。可能的罪魁祸首是:水分从混凝土板中渗透出来，或者至少在更多的实验后看起来是这样。[马提亚斯]还比较了三种不同的除湿机，找到了最好的一种。下面的视频有所有的细节。

我们一直很欣赏[马提亚斯]对这类问题的一丝不苟的态度，以及他在这一领域的权宜之计。他似乎也喜欢他的物质享受——还记得几个月前的目标跟踪空间加热器吗？

 [https://www.youtube.com/embed/pVcbpWrvYns?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/pVcbpWrvYns?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

