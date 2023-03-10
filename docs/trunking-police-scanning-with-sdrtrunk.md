# 使用 SDRTrunk 的中继警方扫描

> 原文：<https://hackaday.com/2020/07/28/trunking-police-scanning-with-sdrtrunk/>

曾经有一段时间，窃听警察和其他服务广播网很容易。警察扫描仪爱好者可以听到现场警察，消防，和救护车的电话。然而，这并不像以前那么容易，因为现在几乎所有的收音机都是集群的。这意味着对话可能会从一个频道跳到另一个频道。然而，P25 可以解读廉价 SDR 加密狗截获的集群无线电通话，并让你监听。[SignalsEverywhere]向您展示如何为 Windows 或 Linux 设置的[，您可以观看下面的视频。](https://www.youtube.com/watch?v=UBrfqLc0E2U)

集群无线电是有意义的。在过去，你可能有十几个不同用途的频道。但是大多数频道大部分时间都是空的。使用中继无线电，无线电的计算机被设置在一个通话组中，控制信道挑选出通话组在任何给定时间应该使用的信道。这意味着一个信道可能具有来自不同通话组的连续几次传输，并且一个通话组可能在每次传输时跳到新的信道。

P25 是用于公共服务集群无线电的 APCO(公共安全通信官员协会)项目 25 标准。当然，你也可以用商业设备来监听这些收音机，但这有什么意思呢？

如今，随着每个人在家的时间越来越多，无线电监听是一种很好的替代生活方式。当然，这不是我们第一次看到 SDR 加密狗扫描仪。请注意[儿童玩具](https://hackaday.com/2011/08/18/project-25-digital-radios-law-enforcemnet-grade-vulnerable-to-the-im-me/)。

 [https://www.youtube.com/embed/UBrfqLc0E2U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/UBrfqLc0E2U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

