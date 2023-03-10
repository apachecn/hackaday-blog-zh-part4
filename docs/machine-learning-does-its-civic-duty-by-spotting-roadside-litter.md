# 机器学习通过发现路边垃圾来履行其公民义务

> 原文：<https://hackaday.com/2022/06/22/machine-learning-does-its-civic-duty-by-spotting-roadside-litter/>

如果有一样东西似乎永远不会受到供应链问题的困扰，那就是垃圾。它无处不在，很容易被发现——你会认为——捡起来。可悲的是，我们大多数人似乎把垃圾当成了别人的问题，但是有了像机器视觉垃圾测绘仪这样的东西，你至少可以成为解决方案的一部分。

对于有公德心的[纳撒尼尔·费莱克]来说，他的家乡圣地亚哥的垃圾问题越来越严重。他认为垃圾所在位置的地图可以帮助市政人员进行清理，因此他着手建立一个自动搜索垃圾的系统。利用 Edge Impulse 和从各种来源捕获的路边图像，他建立了一个识别垃圾的模型。为了找到垃圾，一个安装在车窗上的网络摄像头在驾驶时捕捉图像，一个 Raspberry Pi 4 运行模型并寻找垃圾。当发现路边垃圾时，Pi 使用 Blues 无线记事本通过其蜂窝调制解调器将垃圾的 GPS 位置发送到云数据库。

在圣地亚哥的街道上漫游，纳撒尼尔的系统建立了一个垃圾热点的数据库。从那里，很简单地提取数据并覆盖在谷歌地图上，以创建垃圾所在位置的热图。下面的视频展示了他的系统在运行。

是的，驾驶私人车辆专门寻找垃圾只会增加更多的垃圾，但是你可以想象把这样的东西放在已经在城市中行驶的市政车辆上。不管怎样，我们得到了一些有用的提示，尤其是那些无线物联网卡。[我们在](https://hackaday.com/2021/08/11/a-stress-monitor-designed-specifically-to-help-you-work-from-home/)之前已经见过它们被使用，但是【Nathaniel】的项目为我们提供了一条前进的道路，让我们了解一些已经讨论了一段时间的想法。

 [https://www.youtube.com/embed/RNq5SCukAHM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/RNq5SCukAHM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

