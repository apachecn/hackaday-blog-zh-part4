# 用软件无线电猎狐

> 原文：<https://hackaday.com/2020/12/26/fox-hunting-with-software-defined-radio/>

猎狐，或者说测向，是业余无线电爱好者最喜欢的消遣，无线电操作员在这里尝试对无线电传输的位置进行三角测量。虽然在过去这可能需要大量昂贵的设备，但像大多数业余无线电操作一样，软件定义无线电(SDR)的出现也有助于彻底改变这方面的爱好。[Aaron]向我们展示了如何利用 SDR 进行测向，使用的是他定制的基于 SDR 的 Linux 发行版 DragonOS。

[我们在](https://hackaday.com/2020/04/11/software-defined-radio-made-easy/)之前已经提到过 DragonOS，但是每一次迭代似乎都增加了新的功能。这一次，它包括一个名为 DF-Aggregator 的软件包的实现。该软件(来自[ckoval7])连同 DragonOS 的其余部分被加载到一组(通常至少三个)联网的 Raspberry Pis 上。联网的计算机可以交流关于它们接收的无线电波的信息，并使测向成为这种分布中的另一个有能力的特征。

[Aaron]有几个视频显示了设置和使用它的过程，所有的软件都可以让你自己尝试类似的事情。虽然业余无线电爱好的未来仍不确定，但像这样将经典业余活动引入 SDR 领域的项目确实对复兴业余无线电爱好大有帮助。

 [https://www.youtube.com/embed/bZgPnWVYVRY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/bZgPnWVYVRY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

