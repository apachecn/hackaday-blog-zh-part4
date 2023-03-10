# 你口袋里的是一台 Lisp 机

> 原文：<https://hackaday.com/2018/12/19/thats-a-lisp-machine-in-your-pocket/>

计算机语言总是比计算机硬件发展得更快。一个典型的例子是:我们正在*获取 JavaScript 浮点数的 CPU 指令。20 世纪 70 年代和 80 年代并不是 JavaScript 指令在硅片上的垃圾之火，相反，它们都是关于垃圾收集的。Lisp 机器是为高效运行 Lisp 而设计的 CPU。他们是伟大的，直到负责的公司意识到你必须卖一个产品来维持生意。将一个有趣的建筑与稀有性和历史兴趣结合起来，你就拥有了任何逆向计算爱好者收藏的核心。是的，我们都想要一台 Lisp 机。*

现在有一个关于众包的有趣项目将使这成为可能。这是 MakerLisp 机器，一台信用卡大小的计算机，运行裸机 Lisp。

我们第一次看到 MakerLisp 机器的原始原型是在去年八月的 VCF 西部，当时它还处于非常非常原始的状态。虽然这只是一个原型，但 MakerLisp 名片大小的计算机仍然以 50MHz 运行的 Zilog eZ80 为特色。主板包括一个用于串行连接的 USB 端口和一个用于存储的 microSD 卡插槽。它引导进入 Lisp 环境，你甚至不需要使用 NuBus 卡。我们生活在未来。

因为这是一台信用卡大小的计算机，所以当然有一个扩展板，可以将所有东西都分离出来，包括 GPIOs。作为一个 Z80，你也会得到 CP/M 的支持，但这里真正的故事是 Lisp，在你的口袋里。