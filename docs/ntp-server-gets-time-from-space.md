# NTP 服务器从空间获取时间

> 原文：<https://hackaday.com/2022/01/20/ntp-server-gets-time-from-space/>

廉价的 GPS 单元现在很容易买到，如果你有需要非常精确定位的东西，这是非常好的。然而，寻找物体的位置是 GPS 的众多用途之一。有很多方法可以利用 GPS 用来确定位置的一些辅助工具。在这种情况下，它利用卫星的精确计时能力[建立一个微秒精确的网络时间协议(NTP)服务器](https://austinsnerdythings.com/2021/04/19/microsecond-accurate-ntp-with-a-raspberry-pi-and-pps-gps/)。

GPS 的工作原理是在一个接收器和许多卫星之间进行三角定位，但由于卫星不断移动，因此需要极其精确的定时信号，以便根据所有这些变量准确确定位置。该建筑物简单地从卫星网络中提取时间信息，而忽略位置数据。这个构建只有两个部分，一个廉价的 GPS 接收器和一个 Raspberry Pi，但是[Austin]详细介绍了如何设置软件端，包括安装 PPS、GPSd，然后在 Pi 上设置实际的 NTP 服务器。

虽然如果你没有互联网接入(或者只是想自己做)，这是一种自托管自己的 NTP 服务器的极好方式，但[Austin]确实指出，就准确性而言，这可能在计时方面有些过头了。另一方面，Raspberry Pi 没有自己的内置实时时钟，因此这实际上可能是一种具有成本竞争力的计时方式，即使与 DS3231 RTC 模块等更传统的方式相比。

 [https://www.youtube.com/embed/YfgX7qPeiqQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/YfgX7qPeiqQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

