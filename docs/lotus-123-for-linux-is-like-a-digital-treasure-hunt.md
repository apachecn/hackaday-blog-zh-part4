# Lotus 123 For Linux 就像一次数字寻宝

> 原文：<https://hackaday.com/2022/05/23/lotus-123-for-linux-is-like-a-digital-treasure-hunt/>

听说过*莲花 123* 吗？这是一个统治早期个人电脑市场的古老电子表格程序，从现任 *Visicalc* 手中夺走了桂冠。[塔维斯·奥曼迪]已经设法让[的旧软件在 Linux 下原生运行](https://lock.cmpxchg8b.com/linux123.html)——对于一个有 40 年历史的软件来说，这是一个不小的成就，它原本是为一个不同的操作系统设计的。在下面的视频中，你可以在黑屏上看到绿色的文字。

如果你是一个最近才转向 Linux 的人，你可能不记得“在过去”安装软件是多么痛苦。但是在这种情况下，情况更糟，因为软件甚至不是为 Linux 设计的。整个冒险始于[Tavis]想要找到用来给 *Lotus* 添加插件的 API 工具包。理论上，你可以用它给古老的电子表格程序增加新的功能。

395 美元的软件开发工具包并不常见，而且还有 Unix 版本的 Lotus 123，但是似乎没有人有它的副本。[Tavis]最终找到了一个人，他管理着一个大约 1990 年的 BBS，并且把数据录在了磁带上。原来有一个他可以使用的 SDK 的热拷贝。但是他在论坛的文件列表中注意到了其他东西:久违的 Unix 版本的 *Lotus* ！

一项调查发现，安装程序使用了 TD0 文件，这需要一些研究。幸运的是，有一个实用程序可以将这些文件转换成原始磁盘映像。里面是一个非常大的目标文件。显然，在没有动态加载的日子里，这个对象将与插件模块相链接来安装它们。

目标文件的所有调试信息都是完整的，这使得程序的内部操作更加清晰。旧的可执行文件使用 COFF 格式，但可以重新链接到一个 ELF 文件。当然，这并不简单。[Tavis]写了一个小程序来删除旧式的 Unix 系统调用，这样它们就可以被重新路由到 Linux 系统调用。一些调用只是通过，但其他调用由于结构布局、大小和对齐等方面的差异而需要一些转换。

最后，它都工作了，但没有有效的许可证。然而，[Tavis]觉得既然他有许可证，而且这个软件已经被废弃了，他有权利破解许可证检查。

我们是这里众所周知的滥用电子表格的人。当然，我们[不是唯一的](https://hackaday.com/2021/09/28/excel-ray-tracing-with-help-from-c/)。

 [https://www.youtube.com/embed/hMUhIg9B_So?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/hMUhIg9B_So?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

