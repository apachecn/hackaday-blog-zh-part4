# 重置线路侦探工作的史诗故事

> 原文：<https://hackaday.com/2021/07/31/an-epic-tale-of-reset-line-detective-work/>

在过去的几年里，Pine64 的人们给了我们这么多美味的硬件，但公平地说，他们的产品是给实验者而不是消费者的，因此有时会有点粗糙。例如，他们的集群板是一个迷你 ITX PCB，可以容纳多达 7 个 SOPINE A64 计算模块，并通过板载千兆以太网交换机将它们联网，作为一个集群使用。这是一个名副其实的发电站，但它有一个令人讨厌的缺陷，当被告知时，它似乎不愿意重新启动。[Eric Draken] [开始寻求解决这个问题](https://ericdraken.com/a64-reset-problem/)，当他最终到达那里时，他的进展是一个漫长而引人入胜的阅读。

我们浏览了电路板的内部结构，一路上发现了许多关于复位信号如何产生的信息。最终的罪魁祸首是通过复位分配逻辑本身产生的反电动势，导致低拉线一旦被拉高就永远不会下降到逻辑 0 区域，解决方案是一个极其简单的二极管应用。对于任何希望了解逻辑水平侦探工作的人来说，这是非常值得一看的。与此同时，拥有 28 个 ARM 内核的主板本身似乎有很大的潜力。它甚至是我们之前提到过的个人超级计算机项目中的[的一块板。](https://hackaday.com/2018/03/21/everyone-needs-a-personal-supercomputer/)