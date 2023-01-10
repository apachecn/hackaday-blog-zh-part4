# Raspberry Pi 4 基准测试:32 位与 64 位

> 原文：<https://hackaday.com/2020/01/28/raspberry-pi-4-benchmarks-32-vs-64-bits/>

[Matteo]买了新的树莓 Pi 4。为什么不呢？你会得到一个四核 ARM 处理器，高达 4 GB 的 RAM，以及一个千兆以太网端口，价格为 ~~$35~~ $35-55。然而，默认的操作系统仍然是 32 位系统，没有利用 Pi 4 的 64 位 CPU。所以他安装了一个 64 位 Debian 的简易版本，并为运行 32 位和 64 位操作系统的 Raspberry Pi 4 运行了一些[基准测试。](https://medium.com/@matteocroce/why-you-should-run-a-64-bit-os-on-your-raspberry-pi4-bd5290d48947)

64 位操作系统在几乎所有测试中都表现得更好，这一点也不奇怪。如果有什么令人惊讶的话，那可能就是这种差异如此明显。有些基准测试，比如 Dhrystones，可能与现实生活中的使用没有太大关系。但是有些事情，比如计算散列，可能是您在正常使用中经常做的事情，并且时间差异很明显。

除了 CPU 之外，还有一些东西受到了限制。RAM 速度稍微好一点，但不是很多。丢弃防火墙数据包是另一个很大的区别。32 位系统每秒可以丢弃 268 个包，而 64 位系统每秒可以丢弃 557 个包。VPN 是其他因素限制性能的另一个例子，因此操作系统大小之间的差异并不重要。

基准测试总是很棘手，所以你的里程数——尤其是你的实际里程数——可能会有所不同。然而，抛弃 32 位操作系统确实有一些真正的优势。

如果你对[性能和 Pi 3](https://hackaday.com/2019/07/10/raspberry-pi-4-benchmarks-processor-and-network-performance-makes-it-a-real-desktop-contender/) 性能感兴趣，我们之前已经看过了。剧透提醒:好多了。或者你可以[再往前走](https://hackaday.com/2016/03/01/pi-3-benchmarks-the-marketing-hype-is-true/)，如果你愿意的话。