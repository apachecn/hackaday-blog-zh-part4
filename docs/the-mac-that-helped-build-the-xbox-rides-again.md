# 帮助构建 Xbox 游戏机的 Mac 再次出现

> 原文：<https://hackaday.com/2019/01/24/the-mac-that-helped-build-the-xbox-rides-again/>

微软于 2001 年发布的第一代 Xbox 以其大部分由现成的 PC 组件构建而闻名。凭借定制的奔腾 III CPU 和 IDE 外围设备，该游戏机比之前的任何专用游戏机都更接近当代的台式计算机。如果你仔细想想，这当然很有道理。微软希望使用他们第一次涉足游戏市场时非常熟悉的技术，如果有什么东西比强制系统更新更好的话，那就是 x86 计算机。

但对于他们的后续系统 Xbox 360，微软决定采用他们与 IBM 合作开发的 PowerPC 处理器。这自然意味着他们需要 PowerPC 开发系统给开发者，[这也是微软最终短暂发布 PowerMac G5](https://www.journaldulapin.com/2019/01/21/power-mac-g5-sdk/)的原因。[Pierre Dandumont]拥有了一台古怪的微软品牌的苹果电脑，尽管不幸的是硬盘已经被清空了。但在泄露的驱动器图像和一些硬件调查的帮助下，他现在已经启动并运行了这台机器，就像 2003 年至 2005 年期间微软将它们发送给开发者时一样。

[![](img/e24b84d82da81f04f5b4ac1e873bcbbd.png)](https://hackaday.com/wp-content/uploads/2019/01/xboxdev_detail.png) 既然你是在 Hackaday 上读到这篇文章的，你可能已经猜到这个故事不仅仅是下载一个 ISO 并将其写入 PowerMac G5 的硬盘。显然在社区中有一些关于它是否是微软的某种形式的基本 DRM 的争论，但是无论如何，开发工具包操作系统将只能在具有非常特定的硬件的 G5 上运行。因此，挑战不仅在于弄清楚软件在寻找什么样的硬件，还在于找到它，并在它的全盛时期过去 10 年后安装它。

大多数所需的硬件，如英特尔 741462-010 网卡或 160 GB 希捷 ST3160023AS 硬盘，都很容易在易贝上找到。但棘手的是找到一个苹果版本的 ATi 镭龙 X800 XT。[Pierre]最终得到了一个更常见的 ATi FireGL X3，并将其与 Mac X800 固件一起刷新。这说起来容易做起来难，因为取决于哪家制造商在你的特定显卡上制造了内存，你必须调整时钟速度才能获得可用的图像，但最终他找到了获胜的组合，开发工具包操作系统随着他被黑的显卡启动。

那么，这一切在 2019 年给你带来了什么？[Pierre]承认没什么特别有用的东西，但还是很酷。该系统允许您运行 Xbox 和 Xbox 360 二进制文件，甚至具有旧的 Xbox 360“刀片”风格的仪表板。他说，他在让零售游戏实际运行上只取得了有限的成功，但如果你的目标是在 2019 年运行 Xbox 360 游戏，无论如何肯定有更好的方法来做到这一点。比如买个 Xbox 360。

[我们之前已经讨论过 Xbox 360 相当不寻常的处理器](https://hackaday.com/2018/01/08/speculative-execution-was-a-troublemaker-for-xbox-360/)，但是围绕这些部件，我们更经常[看到的项目是把微软的索福瑞游戏机拆开](https://hackaday.com/2018/09/16/this-xbox-360-is-powered-by-steam/)，而不是探究它实际上是如何工作的。

 [https://www.youtube.com/embed/xG_0RfE-8Jk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/xG_0RfE-8Jk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

