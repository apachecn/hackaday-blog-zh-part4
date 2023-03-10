# LED 时钟将时间分解为光脉冲

> 原文：<https://hackaday.com/2020/04/15/led-clock-strips-time-down-to-pulses-of-light/>

尼采说(本质上)时间是一个扁平的圆——无论我们记不记得，我们都注定要重复历史。这肯定是一个严峻而发人深省的想法，但随着你越来越多地观察[andrei.erdei]将时间从字面上理解为一个扁平的圆圈，这种想法注定会消散。

一个只用 RGB 发光二极管来显示时间的时钟听起来令人困惑，可能会很混乱，但这里的结果非常令人愉快和平静。我们认为它必须是代表 12、3、6 和 9 的较亮 led 和代表其余数字的较暗 led 的组合，加上漫射方案。前板是烟熏丙烯酸，上面有两层磨砂黑窗箔。

在印刷的塑料环内是两个粘性 RGB LED 条，运行在 ESP8266 上，最终连接到 NTP 时间服务器。这些条带是背靠背粘在一起的 60 LED/米长的粘合剂的两个半部分，以便灯交错排列，实现无缝覆盖。这设置了这个时钟最酷的东西——秒针，它由一个粉红色的 LED 灯在环上来回曲折地显示。迷茫？休息后观看简短的演示，你马上就会明白了。

现在时代不同了，你可能对找出今天是什么日子的简单方法更感兴趣。等待结束了。

 [https://www.youtube.com/embed/1w7zy3IAER0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1w7zy3IAER0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

