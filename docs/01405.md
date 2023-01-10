# SDR 是这个汤罐多普勒雷达装置的核心

> 原文：<https://hackaday.com/2018/11/29/sdr-is-at-the-heart-of-this-soup-can-doppler-radar-set/>

想要探索雷达的世界，但又被射频电子的神秘所吓倒？不要再畏首畏尾，通过[Luigi Cruz] 撰写的关于软件定义雷达的教程[来抽象 RF 的复杂性。](https://luigi.ltd/2018-11-23/software-defined-radar-cw-doppler-radar-with-limesdr/)

从我们自己的【Gregory L. Charvat】中获得灵感，他的[许多雷达项目](https://hackaday.com/author/charvatg/)以前曾在我们的页面上出现过，这次投身雷达的预算很少，但却有丰富的学习机会。雷达装置的前端几乎完全包含在 LimeSDR Mini 中，这是一种软件定义的无线电，可以发射和接收。唯一的附加组件是一对汤罐天线和一个用于接收端的廉价 LNA。系统的其余部分运行在运行于 Raspberry Pi 上的 GNU Radio Companion 上；整个装置由一个 USB 电池组供电，放在一个塑料手提包里。[Luigi]为 2.4 GHz ISM 频段设置了雷达，下面的视频显示它正在与以已知速度驶过的车辆进行校准。

诚然，LimeSDR 并不便宜，但它的性价比很高，降低了进入雷达领域的主要障碍。而且[Luigi]在记录他的工作和[让他的代码可用](https://github.com/luigifreitas/software-radar)方面做得很好，这也会有所帮助。

 [https://www.youtube.com/embed/uB6TDklbbI4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/uB6TDklbbI4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

