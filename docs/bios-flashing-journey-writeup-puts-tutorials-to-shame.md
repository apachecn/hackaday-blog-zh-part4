# BIOS 闪烁之旅写的自惭形秽教程

> 原文：<https://hackaday.com/2021/12/26/bios-flashing-journey-writeup-puts-tutorials-to-shame/>

几周前，[道格·布朗]买了一个锐龙主板，宣传为“不工作”，并相应地打折。他注意到卖家没有用任何足够旧的 CPU 来测试它，以支持主板的 BIOS 版本[，并决定冒险升级它](https://www.downtowndougbrown.com/2021/12/upgrading-a-motherboards-bios-uefi-the-hard-way/)。

由于手中也没有受支持的 CPU，他决定走“外部程序员”的路线，这条路线获得了成功，并给了这个主板一个新的生命。然而，这不是我们写这篇文章的原因。这篇文章引起我们注意的原因是因为[道格]的研究不遗余力，而且都有值得学习的地方。无论是通过仔细的观察还是彻底的研究，这篇文章涵盖了所有的要点以及更多的内容，作为任何想要编写 BIOS 的人的学习榜样。

例如，【Doug】正确地指出了[这些普通程序员](https://www.chucknemeth.com/usb-devices/ch341a/3v-ch341a-mod)的一个设计问题，该问题导致 5 V 电压接入 3.3 V 数据线，并通过重新布线电路板解决了这个问题。查看 ICs 零件号中的所有字母，这是我们许多人会忽略的东西，[Doug]注意到闪存芯片只有 1.8 V，并采购了 1.8 V 适配器以避免烧毁他的主板的可能性。在发现 1.8 V 适配器不适用于某些人后，他逆向工程了适配器的原理图，并确认它确实应该与他收到的适配器上的特定部件一起工作。

注意到零件号中的另一个字母暗示闪存芯片可能配置为四 SPI 操作，他添加了串联电阻，以确保程序员没有机会用硬连线引脚损坏 BIOS 芯片。这只是[Doug]文章中见解的一个例子，为了简洁起见，还有更多我们不能提及的，我们鼓励你自己去看看。

在这个过程中投入了如此多的关注，修改成功也就不足为奇了。这里分享的这种求知欲是值得向往的，这样的文章在洞察力和有用性方面经常超过通用教程。你有什么“成功地利用了不工作的东西”的故事？

如果你正在寻找其他有见地的 BIOS 故事，我们已经报道了有人[对他们的 BIOS 进行逆向工程，以删除 miniPCIe 卡白名单](https://hackaday.com/2021/08/23/school-surplus-laptop-bios-hacked-to-remove-hardware-restrictions/)。我们通常报道笔记本电脑中的 BIOS 修改故事，因为修改它们有更多的动机，但许多笔记本电脑 BIOS 文章也适用于台式机主板，例如这个[管理员密码删除故事](https://hackaday.com/2021/03/24/removing-supervisor-passwords-and-learning-python/)或我们自己的【汤姆·纳尔迪】的这个 [LibreBoot 安装之旅](https://hackaday.com/2018/08/20/installing-libreboot-the-very-lazy-way/)。

感谢[Sidney]与我们分享这些！