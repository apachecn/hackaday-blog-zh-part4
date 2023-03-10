# 更多使用 DragonOS 的软件定义无线电项目

> 原文：<https://hackaday.com/2021/11/03/more-software-defined-radio-projects-using-dragonos/>

DragonOS 是一个基于 Debian 的 Linux 发行版，专门为软件定义的无线电功能打包，在去年疫情各种封锁开始时，它在波长上咆哮。自那以后，该操作系统的创造者[Aaron]一直忙于向发行版添加功能，并制作大量视频来展示其功能，同时也为可能想了解软件定义无线电的人提供操作指南。[最新的是一个关于使用这个软件在某些指定的频谱中检测无线电信号的视频](https://www.youtube.com/watch?v=3xzODzRBuRA)。

这种构建使用两个 RTL-SDR 器件与 DragonOS 软件套件配对，以自动检测特定频率范围内的活动频率，以及超过平均噪底以上的阈值。该视频包括软件的设置及其在检测这些信号中的使用，还包括提供记录功能的 influxdb 和 Grafana 的设置。使用这种设置，本地或互联网上的多个接收器可以配置为将所有识别的频率、功率和时间戳转储到 DragonOS 中。

[Aaron]还一直在帮助开发人员构建包含 GPS 支持的 [SDR4space.lite](https://www.rtl-sdr.com/dragonos-automated-spectrum-analysis-with-sdr4space-lite/) 应用程序，因此他希望在未来的视频中，用户能够轻松地将位置与识别的频率相关联。像这样的项目也提醒人们，进入软件定义的无线电就像买一个 10 美元的 USB 无线电接收器和配置一些免费软件来做任何你可以想象的事情一样简单[比如实时跟踪船只和飞机](https://hackaday.com/2020/10/22/tracking-boats-and-ships-in-real-time-at-the-same-time/)。

 [https://www.youtube.com/embed/3xzODzRBuRA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/3xzODzRBuRA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

