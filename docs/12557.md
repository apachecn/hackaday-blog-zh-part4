# 是月亮爬进了你的电脑吗？

> 原文：<https://hackaday.com/2022/01/23/is-that-the-moon-worming-its-way-into-your-bios/>

当面临恶意软件的情况时，通常的“保证解决方案”是重新安装您的操作系统。[恶意软件世界的新发展](https://securelist.com/moonbounce-the-dark-side-of-uefi-firmware/105468/)也要求你身边有一个 CH341 程序员。在一个可以说是不可避免的发展中，[卡巴斯基实验室]的研究人员发现了一个活跃的恶意软件，它将通过将其引导代码写入 BIOS 芯片来保持自身。如果你撕碎硬盘并换上新的也没关系。事实上，所谓的 MoonBounce 从来没有真正接触过磁盘，只是小心地将自己存储在 RAM 中，哦，当然还有存储 BIOS 代码的 SPI 闪存。

MoonBounce 是微软定制的，能够挂钩到一个组件链，从 UEFI 的 DXE 环境开始，通过 Windows Loader，最后作为`svchost.exe`的一部分，这是一个我们都知道并喜欢的过程。

这种方法似乎还没有普及，但不难想象，我们最终会遇到一种勒索病毒，利用这种方法来赚点外快。接下来会发生什么——BIOS 在我们的路边刷新服务卡车？毕竟，您的主板内置 BIOS flasher UI 内置在同一个 BIOS 映像中，该映像会受到损害，最好的情况是，可以毫不费力地被禁用——最糟糕的情况是，被破坏并用于进一步偷偷摸摸的持续存在，愚弄维修人员，使其感到舒适，但一周后却又出现了一个 Monero 地址。

随着所有的测试剪辑摆弄和 SOIC-8 拆焊成为我们中很大一部分人的第二天性，我们的硬件黑客技能会突然变得受欢迎吗？我们应该储备 CH341 加密狗吗？这么多问题！

本周的“可能很快变得流行的威胁媒介”是一个有趣的推测！想了解我们可能没有足够重视的其他媒介吗？供应链对我们仓库的攻击不会错的！至于其他基于辅助存储的持久化方法，请查看[这款嵌入硬盘固件的概念验证 rootkit](https://hackaday.com/2015/06/08/hard-drive-rootkit-is-frighteningly-persistent/) 。当然，我们可能并不总是需要新奇的方法来做事，老方法仍然经常有效——你可能只需要[将你的恶意硬件伪装成一个很酷的笔记本电脑配件](https://hackaday.com/2018/07/11/teardown-of-usb-fan-reveals-journalists-lack-of-opsec/)来欺骗一个普通的记者，即使是在一个充满敌意的环境中。

感谢 Brendan Dolan-Gavitt 在 Twitter 上向我们强调了这一点！

主图[由卡巴斯基实验室](https://securelist.com/moonbounce-the-dark-side-of-uefi-firmware/105468/)提供。