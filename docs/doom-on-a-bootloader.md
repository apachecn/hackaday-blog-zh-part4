# Bootloader 上的 DOOM 是终极欺骗代码

> 原文：<https://hackaday.com/2021/04/16/doom-on-a-bootloader/>

将 DOOM 移植到并不意味着要运行它的硬件上是一个由来已久的传统。让它在嵌入式设备、古老的计算机、虚拟计算机和古董视频游戏机上运行都是经典的技巧，但 DOOM ports 一直在等待的是具有普遍适用性的东西，不需要为每件硬件定制解决方案。类似 DOOM 的东西在引导装载程序中运行。

[Ahmad]使用的引导程序叫做 Barebox，主要用于嵌入式系统，通常是运行 Linux 的系统。这是直接访问硬件的完美环境，因为引导装载程序兼作裸机硬件启动工具包。既然 DOOM 运行在这个引导加载程序上，它可以有效地运行在从嵌入式设备到笔记本电脑的任何地方，只需做最少的工作，虽然在引导加载程序中运行它可以消除通常需要在移植过程中完成的大量艰苦工作，但它可能仍然需要对不支持的特定硬件进行一些调整。

对于那些已经运行 Barebox 的人来说，bareDOOM 代码可以在[【Ahmad】的 GitHub 页面](https://github.com/a3f/bareDOOM/)上找到。对于那些没有运行 [Barebox](https://www.barebox.org/) 的人来说，与其他引导程序相比，它确实有很多好处，甚至除了它玩经典 FPS 游戏的新功能。对于那些喜欢更定制的毁灭战士设置的人来说，我们永远是在 NES 弹药筒中运行的[毁灭战士的粉丝。](https://hackaday.com/2019/08/29/how-to-play-doom-and-more-on-an-nes/)

图片: [AntonioMDA，CC BY-SA 4.0 通过维基媒体共享](https://commons.wikimedia.org/wiki/File:Brutal_Doom.jpg)