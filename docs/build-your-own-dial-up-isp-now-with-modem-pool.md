# 建立自己的拨号上网服务提供商-现在与调制解调器池！

> 原文：<https://hackaday.com/2020/05/30/build-your-own-dial-up-isp-now-with-modem-pool/>

当它是唯一可行的选择时，拨号上网的刺耳尖叫对许多人来说是一件不受欢迎的头痛事。但现在它的时代已经过去，它获得了某种怀旧情绪，使它受到今天技术爱好者的喜爱。[Doge Microsystems]就是这样一个人，他全力以赴为多个客户开发他们自己的拨号网络服务提供商。

[![](img/0e9940c3ed604d222302c0a18f57a778.png)](https://hackaday.com/wp-content/uploads/2020/05/isp4800.jpg) 复古网络[基于更早的单设备实验](https://hackaday.com/2019/02/16/build-your-own-dial-up-isp-with-a-raspberry-pi/)，用树莓派 3B 充当拨号服务器。它连接到四个调制解调器，其中三个通过 USB 串行适配器连接，实现硬件流控制。

显然，在这个时代很难找到四条模拟电话线，所以[Doge]使用 Asterisk 和一系列 Linksys SIP 设备来创建他们自己的 PBX 网络。每个调制解调器都有一条电话线，剩下四条供客户拨入。

要进行连接，用户可以直接呼叫某个调制解调器，或者拨打一个特殊的号码，这个号码会响遍整个池。多亏了`mgetty`，每个调制解调器都被设置成在不同的响铃次数上应答，以分担负载。一旦连接，PPP 守护进程将处理用户与整个互联网的连接。

虽然我们不太可能都打电话到[Doge]家去获取下一个 YouTube 补丁，但拥有自己的拨号网络服务提供商无疑是一个令人钦佩的壮举。我们希望看到它在某个时候被部署到现场，也许是在黑客会议或燃烧人类型的活动上。当然，如果你有自己的老派网络抽取数据，一定要让我们知道！休息后的视频。

> 我的新的自己动手拨号 ISP 指南终于准备好了，现在有了一个供多个客户使用的调制解调器池！[https://t.co/lVnZK0mhtN](https://t.co/lVnZK0mhtN)
> 
> 这次我甚至买了一个 USB 调制解调器:)[pic.twitter.com/bhr8ffKnb0](https://t.co/bhr8ffKnb0)
> 
> — Doge 微系统(@ DogeMicrosys)[2020 年 5 月 30 日](https://twitter.com/DogeMicrosys/status/1266735344843661312?ref_src=twsrc%5Etfw)