# 尝试在计算模块 4 中使用 GPU(但失败了)

> 原文：<https://hackaday.com/2020/11/10/trying-and-failing-to-use-gpus-with-the-compute-module-4/>

随着每一次迭代，Raspberry Pi 平台变得更加强大。尽管如此，它们仍然不是高性能计算的首选，而且由于成本和范围的原因，它们的外部接口也是有限的。尽管如此，像杰夫·格尔林这样的人还是努力定期将平台推向极限。不幸的是，[[Jeff]最近的 GPU 实验遇到了一个他至今无法克服的困难。](https://www.youtube.com/watch?v=ikpgZu6kLKE)

随着新的计算模块 4 的发布，Raspberry Pi 生态系统现在有一个具有 PCI-Express 2.0 1x 接口的设备作为库存。这导致了许多质疑，GPU 是否可以与硬件一起使用。[Jeff]决心找出答案，购买了一对较旧的 ATI 和 NVIDIA GPUs 来玩。

直接结果令人失望，插入模块后没有任何输出。当然，[Jeff]并不期望事情是即插即用的，所以深入内核消息以找出问题所在。第一个问题是 Pi 有限的基址空间；GPU 需要在 BAR 中分配大量内存才能工作。随着 CM4 的 BAR 从 64MB 扩展到 1GB，这些卡似乎可以被正确识别，并且可以安装 ARM 驱动程序。

唉，故事到目前为止没有成功。NVIDIA 和 ATI 驱动程序都无法正确初始化卡。后一个驱动程序抛出了一个错误，因为 Raspberry Pi 未能考虑 I/O BAR 空间，这是一个遗留的 x86 特性，[，但其他人认为问题可能出在其他地方](https://github.com/geerlingguy/raspberry-pi-pcie-devices/issues/4#issuecomment-719989424)。虽然[Jeff]可能还没有完成这一壮举，但他已经接近了，我们怀疑再多做一点工作，社区就会找到解决方案。鉴于这些 GPU 的 ARM 驱动程序的存在，我们确信这只是一个时间问题。

有关计算模块 4 的更多信息，[请查看我们的综合文章](https://hackaday.com/2020/10/19/new-raspberry-pi-4-compute-module-so-long-so-dimm-hello-pcie/)。休息后的视频。

 [https://www.youtube.com/embed/ikpgZu6kLKE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ikpgZu6kLKE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

