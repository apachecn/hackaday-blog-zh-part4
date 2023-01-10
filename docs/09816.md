# 最新的 PlayStation Exploit 跳过光盘

> 原文：<https://hackaday.com/2021/04/10/newest-playstation-exploit-skips-the-disc/>

上个月，我们为您带来了 tonyhax 的消息，这是最初的索尼 PlayStation 的一个聪明的利用，它利用了*托尼·霍克职业滑板者*系列的几个游戏中的缓冲区溢出，从一个特别准备的存储卡中加载任意代码。但是现在[Bradlin]将这个想法推进了一步，[为索尼标志性的控制台开发了一个软件漏洞，不需要从游戏](https://github.com/brad-lin/FreePSXBoot)中触发。

这次的漏洞利用要复杂得多，但是[Bradlin] [为那些想要更多细节的人做了出色的工作。简而言之，PlayStation 内置存储卡处理例程中缺少边界检查，这意味着存储卡上精心格式化的“块”可以让控制台执行一个 128 字节的小有效载荷。这并没有太大的空间，但它最终足以加载存储在存储卡上其他地方的额外代码，并真正开始工作。](https://github.com/brad-lin/FreePSXBoot/blob/master/exploit/EXPLOIT.md)

与 tonyhax 不同，它是专门设计来允许用户用刻录到 CD-R 的游戏来交换他们的零售*托尼·霍克*光盘的，【Bradlin】的 FreePSXBoot 更像是一个通用的加载程序。就目前而言，它不允许你实际上玩烧毁的游戏，尽管不可避免的是，有人会很快将最后几个点连接起来。

如果你想查看目前为止的进展，你只需要将 PlayStation 存储卡连接到 Arduino，将提供的图像写入其中，然后将其插入插槽中。[Bradlin]说这个漏洞并不是 100%的时候都有效(其他的事情肯定会在未来的版本中解决)，但是在你看到闪烁的屏幕之前，不应该尝试太多,[证明索尼 27 岁的主机现在已经真正被打败了](https://hackaday.com/2018/11/05/how-the-sony-playstation-was-hacked/)。

 [https://www.youtube.com/embed/29DI-N45V40?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/29DI-N45V40?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

