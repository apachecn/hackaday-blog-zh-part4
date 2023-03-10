# 微软发布皇冠上的宝石——从 1982 年开始！

> 原文：<https://hackaday.com/2018/10/01/microsoft-releases-crown-jewels-from-1982/>

如果你回顾大约 30 年前，不清楚个人电脑会发生什么。然而，大多数人都相信 CP/M——来自数字研究的操作系统——会继续增长，并为任何可用的新机器提供动力。但事实并非如此。MS-DOS 接管了这个词，并最终导致了我们今天所知的大量 Windows 电脑。微软在 GitHub 上发布了[到 MS-DOS 1.25 和 2.0 的源代码。](https://github.com/Microsoft/MS-DOS)

微软——当时另一家羽翼未丰的计算机公司——写了一些基本的解释程序，并想进入操作系统领域。他们向西雅图计算机产品公司支付了 75，000 美元的巨款，购买由蒂姆·帕特森写的 qdo。更名为 MS-DOS，第一个版本出现在 1981 年末，1.25 版本在大约一年后推出。

虽然你可能认为拥有 MS-DOS 源代码没什么大不了的，但 DOS 仍然有很多生命力，从教育和历史的角度来看，这也很有趣。如果您不想阅读 x86 汇编语言，也有示例的基本源代码(矛盾的是，在 bin 子目录中)以及为 EDLIN 和 DEBUG 等老朋友编译的 COM 文件。

特别感兴趣的是非常小的汇编源代码。还有将 Z80 代码转换成 x86 代码的源代码，这可能很有趣。不过，要注意。该文件的 1200 行中没有多少注释。

版本 2.0 的源代码有更多的文件，包括 EDLIN 和 DEBUG 之类的源代码。我们想知道 1.25 版本的文件是否丢失，太难看而无法显示，或者 COM 文件是否是手工编码的？

如果你在 1990 年告诉我们微软将开放源代码 MS-DOS，我们会让你承诺。他们在自述文件中用这一小段展示了他们的幽默感:

> 此回购中的源文件用于历史参考，将保持静态，因此请不要发送建议对源文件进行任何修改的拉请求，…

如果这让你想写一些新的 DOS 程序，你现在可以[实际上使用 GCC](https://hackaday.com/2018/05/14/msdos-development-with-gcc/)。或者你想扮演驴子。BAS 文件， [QB64](https://hackaday.com/2018/02/22/quickbasic-lives-on-with-qb64/) 大概可以。