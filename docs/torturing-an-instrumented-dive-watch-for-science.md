# 为了科学而折磨装有仪器的潜水表

> 原文：<https://hackaday.com/2019/07/18/torturing-an-instrumented-dive-watch-for-science/>

互联网是一个狂野多变的地方，人们可以肆无忌惮地谈论任何事情。如果你听起来像是知道自己在说什么，并抛出一些适当的行话，那么很有可能有人会相信你在卖什么。

例证:那些声称 300 米潜水手表会漏水，如果你在淋浴时晃动它们太多。看起来很荒谬，但是克里斯托夫·马西尼亚克并没有拒绝这种说法，而是选择用一个塞在潜水表盒里的微型无线压力传感器来证明这一点。当他的目光落在他工作台上手表旁边的 ESP-01 模块上时，他产生了这个想法。他认为这两个人需要聚在一起，于是订购了一个 BMP280 压力传感器板，足够小，可以放在任何地方。在一个小型脂肪包的配合下，所有东西都被塞进了一个因维克塔潜水手表盒。添加了一点代码来记录温度和压力，并通过 WiFi 传输结果，[Kristopher]开始对他的设置进行折磨测试。

第一个有趣的结果是传感器的灵敏度有多高，以及温度的微小变化对外壳内部压力的影响有多大。手表在压力容器中模拟潜水到 70 米，这只是略微增加了内部压力，并用 2300 磅/平方英寸(16 兆帕)的压力清洗机进行了剥皮式淋浴，也只有最小的影响。下面的视频展示了结果，但带回家的信息是，在淋浴时漏水的潜水表不算是潜水表。

向[克里斯托弗]致敬，感谢他在这里所做的工作。我们总是喜欢像这样的公民科学努力，无论是[无硬件射电天文学](https://hackaday.com/2016/08/30/citizen-scientist-radio-astronomy-and-more-no-hardware-required/#more-218476)还是[用无人机采样鲸鱼鼻涕](https://hackaday.com/2018/08/01/hanky-deprived-drones-taste-whale-snot-for-science/)。

 [https://www.youtube.com/embed/41HYLJL1eCc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/41HYLJL1eCc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

