# 用于 Pi 的 10 千兆以太网

> 原文：<https://hackaday.com/2021/07/09/10-gigabit-ethernet-for-the-pi/>

当像贝尔和马可尼这样的人发明电话和无线电时，你不得不怀疑他们找谁进行测试。毕竟，他们有了第一台设备。[杰夫]也有类似的问题。他得到了一个使用 Raspberry Pi 计算模块的 10 千兆网卡。但他没有任何其他快速设备可以交谈。简单吧？只需要一个路由器和另一个网卡。[Jeff]我也是这么想的，但正如你在下面的视频中看到的，这并不那么容易。

诚然，一些(但不是全部)抢劫是自己造成的。例如，做一些金属加工，将一些齿轮放入 19 英寸的机架中。然而，有些问题是不可避免的，例如路由器有 10 Gbps 端口，但没有足够的吞吐量来以该速度传输流量。重新布线也是一项艰巨的任务。

很多工作都围绕着一些枝节问题，如风扇噪音和将 StarLink 添加到网络中，这些并没有真正提高速度，但我们理解项目中的干扰。

路由器不是唯一不能处理整个 10 Gbps 数据流的设备。Pi 本身有一个 4 Gbps 的 PCI 通道，因此您最多可以获得 4 Gbps，测试表明实际限制不是 3.6 Gbps。这仍然令人印象深刻，网卡卸载也有助于 PI 的性能。

另外，如果你曾经尝试过自己制作视频，看看视频结尾的剪辑可能会让你对自己的努力感觉更好。我们肯定都有同样的问题。

如果你想便宜地升级到 10Gb 网络，[我们有一些建议](https://hackaday.com/2019/07/24/doing-10-gigabit-networking-at-home-the-cheap-way/)。只是小心不要让[在线缆上精打细算](https://hackaday.com/2016/01/30/is-your-cat-6-ethernet-cable-cat-6-probably-not/)。

 [https://www.youtube.com/embed/FTP5h9jnVx0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/FTP5h9jnVx0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

