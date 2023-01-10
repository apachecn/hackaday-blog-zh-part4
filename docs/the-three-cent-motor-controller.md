# 三分电机控制器

> 原文：<https://hackaday.com/2021/12/29/the-three-cent-motor-controller/>

如果你关注小型微控制器的世界，你肯定会熟悉 Atmel、ARM Cortex、PIC 等常见产品。但这些都不是最小或最便宜的设备，在它们下面是一整个类别的微尘微控制器，具有最小的能力和最低的价格。也许最著名的是红木系列芯片，其类似 PIC12 的架构只需几便士就能买到。这些是著名的 3 美分微控制器，但是尽管它们很有名，但在我们的社区中它们还是有点难以合作的名声。[Ben Lim]通过 Padauk 消除了其中一些想法,[用打印机中的电机和编码器制作一个三分电机控制器](https://westsideelectronics.com/repurposing-the-encoder-counter/)。

红木没有 SPI 等片上外设，相反，它的 IDE 提供了位碰撞代码来完成这项工作。这个和一些 PID 电机控制器代码在这个小芯片上完成了一项简单的任务，在可能更贵的 MAX14870 的帮助下，它可以驱动电机。出于好奇，[代码可以在 Git Hub 仓库](https://github.com/benlhy/Padauk/tree/master/MotorController)中找到。可能会有更多的电机控制器被发现，但我们怀疑你会找到一个更便宜的微控制器。

想知道红木有什么大惊小怪的吗？[我们的同事【Maya Posch】为您报道了](https://hackaday.com/2019/09/09/everything-you-wanted-to-know-about-padauk-mcus-and-more/)。