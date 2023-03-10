# Chumby 很快会有新的内核

> 原文：<https://hackaday.com/2022/12/21/chumby-gets-new-kernel-soon/>

如果你错过了查比，我们很抱歉。它们是相对便宜的 Linux 设备，充当时钟、网络收音机和 feed 阅读器。该公司破产了，尽管由于一位创始人的努力，还保留了一些功能，现在，只要支付订阅费，你仍然可以让你的 Chumby 继续运营。然而，[Doug Brown]买了一个，目的是将其用于自己的应用。但是 2.6.28 内核已经显老了。所以他决定在设备上推一个[新内核。](https://www.downtowndougbrown.com/2022/12/upgrading-my-old-chumby-8-linux-kernel-part-1-u-boot/)

如果你是一个 Chumby 爱好者，不要太激动。我们的目标不是为现有的 Chumby 应用程序提供一个新的内核，[道格]说这可能是不可能的。相反，他希望在设备上为自己的软件安装一个现代化的引导基础设施和内核。

这篇文章只是第一部分，但它涵盖了他如何让 U-Boot 从 SD 卡加载。鉴于这方面的成功，我们认为新内核运行的时间不会太长。

理解启动过程是一个有点晦涩难懂的知识，早在 2013 年[Doug]就发现他对它的理解还不足以让 3.13 内核在机器上运行，但现在他已经准备好接受挑战，根据他迄今为止的工作，我们同意这一点。

当 Chumby [停止销售硬件](https://hackaday.com/2012/04/21/chumby-is-no-longer-selling-hardware/)时，我们很难过。Chumby 也给其他公司贴了这个设备的白色标签，我们看到至少其中一个[在驾驶一个机器人](https://hackaday.com/2011/08/29/chumby-controlled-mechanum-wheel-robot/)。