# 以太网通向以太网

> 原文：<https://hackaday.com/2020/11/09/ethernet-goes-to-the-ether/>

由于以太是一个古老的术语，指的是无线电波传播的虚拟空间，我们一直认为以太网这个术语指的是有线通信很奇怪。当然，有无线设备，但那不是真正的以太网。[亚采克]也有同样的想法，但决定[对此做点什么](https://lipkowski.com/etherify/)。

他所做的是使用两种不同的技术来改变 Raspberry Pi 上以太网适配器的电磁发射。不同的条件发送莫尔斯电码，你可以用合适的接收器以 125 兆赫接收。

实用？很难，除非你想从一台有气隙的机器中获取数据。但它确实有一定的酷的因素。第一种方法是在 10 Mbps 和 100 Mbps 之间切换适配器。第二种技术使用数据流来完成调制。切换方法的范围约为 100 米，而基于数据的方法最高可达 30 米。如果你想复制这个实验，代码在 [GitHub](https://github.com/sq5bpf/etherify) 上。

这种事情有很多先例。1976 年，多布博士的杂志发表了一篇文章，内容是在附近有调幅收音机的情况下，通过运行代码在 Altair 8800 上播放音乐。[我们已经看到 VGA 适配器也被迫传输数据](https://hackaday.com/2018/04/23/spoofing-cell-networks-with-a-usb-to-vga-adapter/)。

 [https://www.youtube.com/embed/ueC4SLPrtNg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ueC4SLPrtNg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/ueC4SLPrtNg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ueC4SLPrtNg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

