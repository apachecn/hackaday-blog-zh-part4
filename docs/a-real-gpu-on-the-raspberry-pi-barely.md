# 树莓 Pi 上的真正 GPU 勉强。

> 原文：<https://hackaday.com/2022/04/28/a-real-gpu-on-the-raspberry-pi-barely/>

[Jeff Geerling]看到了 Raspberry Pi 计算模块 4 及其暴露的 PCI-Express 1x 连接，很自然地想知道他是否可以将 GPU 插入该插槽并使其工作。它没有。原因有几个，比如有限的基址寄存器空间，以及不是为 ARM 硬件编写的驱动程序。在 Raspberry Pi 软件工程师和其他 Linux 内核黑客的帮助下，这些问题得到了解决，尽管在 CPU 方面有很大的障碍。Pi 4 中的 Broadcom 芯片 BCM2711 有一个不完整的 PCIe 实现。

终于有了突破——多亏了围绕这个主题涌现的专门社区，一组内核补丁设法解决了硬件问题。现在可以在 Raspberry Pi 4 计算模块上运行镭龙 HD 5000/6000/7000 卡。仍然有一些小故障，使这一工作的内核补丁可能永远不会登陆上游。也就是说，可以在 Pi 上的镭龙 GPU 上运行桌面环境，甚至一些简单的基准测试。结果…并不特别鼓舞人心，但那真的不是重点。您可能会问，Pi 上的全尺寸 GPU 有什么实际用途。当然，可能是加密挖掘或仿真，或者能够为数字标牌运行更多监视器。不仅如此，它可能有助于确保下一个 Pi 有一个有效的 PCIe 实现。但就像我们在这里讨论的许多事情一样，真正的原因是这是一个一群爱好者无法独自面对的挑战。

 [https://www.youtube.com/embed/crnEygp4C6g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/crnEygp4C6g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

