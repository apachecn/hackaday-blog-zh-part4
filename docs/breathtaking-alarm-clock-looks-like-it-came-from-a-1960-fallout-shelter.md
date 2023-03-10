# 令人惊叹的闹钟看起来像是来自 1960 年的辐射掩蔽所

> 原文：<https://hackaday.com/2020/08/10/breathtaking-alarm-clock-looks-like-it-came-from-a-1960-fallout-shelter/>

所有的铁杆极客都有闹钟，其中的撞钟是一个硬盘读取头…或者至少他们会在看到这个之后建造它们。【老年数据系统】用十进制计数器创造了[一个工业电压闹钟，看起来像是从一个防辐射掩体中出土的(](http://tempect.de/senil/uhr.html)[机器翻译](https://translate.google.com/translate?sl=auto&tl=en&u=http%3A%2F%2Ftempect.de%2Fsenil%2Fuhr.html))。

乍看之下，你可能会误以为这是一个二进制时钟，因为它使用一列发光二极管来表示 24 小时制时间的每个数字。事实并非如此，因为每行对应于 CD4017 十进制计数器上的一个引脚，这些计数器构成了内部的计时电路。

拇指~~螺丝~~在笨重的手持设备顶部的轮子开关是如何设置闹钟时间的，沿着顶部边缘触发一个铃。该时钟由 50 Hz 线路电压驱动，并且[SDS]尝试使用该交流电驱动螺线管作为原型装置上的撞针，但其性能很差。正如在休息后的视频中所听到的，使用硬盘读取头被证明是完美的前锋。至于从十进制计数器触发，下面是[SDS]告诉我们的设计:

> 开关的输出与 10 赫兹的信号进行“与”运算(在 60 赫兹的电网上，它将变为 12 赫兹)。这就驱动了一个稍显粗壮的晶体管，晶体管又驱动了一个电磁铁去敲打一个铃，这个铃把我的自行车弄坏了。是的。这是一个数字模拟闹钟。时钟部分是数字的，但铃声是模拟的，听起来像祖父的旧发条闹钟。

当 600 多个工业发光二极管(24v-48v)的缓存落入他的手中时，这个构建就产生了。当点对点焊接连接面板安装灯和所有九个逻辑芯片时，这使得时钟的内部变得引人注目。加上获得线路电压的变压器，我们想象这东西有相当大的分量。

如果你曾经有过上紧发条的闹钟，你就会知道没有比这更好的方式将你从平静的睡眠中唤醒，进入混乱的现实世界。如果硬盘磁头的轻微叮当声对你来说还不够的话，[这款 fire bell 闹钟肯定能满足你的要求](https://hackaday.com/2013/11/03/fire-bell-wakes-you-for-work-by-shaving-years-off-your-life/)。

 [https://www.youtube.com/embed/ja9K4hA7UwM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ja9K4hA7UwM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

