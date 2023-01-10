# Raspberry Pi 处理器更新中有什么？

> 原文：<https://hackaday.com/2021/09/30/whats-in-a-raspberry-pi-processor-update/>

我们这些多年来一直关注 Raspberry Pi 的人将会熟悉 little board 的各种版本，以及随之而来的新处理器。可能不太明显的是，在任何芯片的生命周期内，通常会有较小的版本变化，通常是为了修复错误或微调生产流程。它们是同一个芯片，但有时有一些额外的功能。[Jeff Geerling] [没有错过这一点，当时 Raspberry Pi 400 有一个版本号比 Pi 4](https://www.jeffgeerling.com/blog/2021/raspberry-pi-4-model-bs-arriving-newer-c0-stepping) 更新的 BCM2711，现在他注意到 Pi 4 板上有相同的芯片。

为什么他们会同时运行两个不同版本的芯片呢？似乎更新改变了 eMMC 和 PCIe 总线可寻址的内存量，前者只能看到前 1GB，后者只能看到前 3Gb。对于较低规格的 Pi 4 板来说，这并不存在问题，但对于那些 8g 内存的板来说，这显然是一个问题。因此，Pi 400 和顶级规格 Pi 4 现在有了更新的 BCM2711 版本。对于普通的 Raspberry Pi 操作系统用户来说，这几乎肯定不会被注意到，但对于希望暴露 PCIe 总线并与 GPU 等外设进行对话的硬件实验人员来说，额外的内存寻址空间应该会引起他们的兴趣。也就是说，尽管他暗示计算模块 4 有更新的版本，但他自己的实验并不成功。

[编者按:[我们自己的超频实验](https://hackaday.com/2020/11/11/adventures-in-overclocking-which-raspberry-pi-4-flavor-is-fastest/)显示 C 版 SOC 比 B 版运行得更冷/更快，因此在“正常”的 Pi 外形中拥有更好的芯片而不仅仅是 Pi 400 和计算模块是很好的。]