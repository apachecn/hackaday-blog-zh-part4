# 撒旦把硬盘电缆变成天线，以击败空气间隙安全

> 原文：<https://hackaday.com/2022/07/22/satan-turns-hard-drive-cable-into-antenna-to-defeat-air-gapped-security/>

本古里安大学(Ben-Gurion University)的莫迪凯古里(Mordechai Guri)实验室似乎是空气隙计算机死亡的地方，或者至少是泄露其秘密的地方。并且[这种利用计算机的 SATA 电缆作为天线](https://arxiv.org/abs/2207.07413)来窃取数据的黑客行为是典型的个人电脑可以进行多少旁路攻击的另一个例子。

这个漏洞被巧妙地命名为“撒旦”，它依赖于许多计算机中使用的 SATA 3.0 接口具有 6.0 Gb/s 的带宽，这意味着操纵计算机的 IO 将有可能以大约 6 GHz 的频率从空气隙机器传输数据。当然，这是一个复杂的利用，包括使用通常的方法在目标机器上放置一个传输程序，如网络钓鱼或零日利用。一旦到位，传输程序就使用 SATA 磁盘上的读写操作的组合来生成对要泄露的数据进行编码的 RF 信号，SATA 电缆内的数据线充当天线。

下面的视频展示了撒旦的行动。传输仅仅几个字节的数据需要一段时间，而且范围不到一米，但这足以让该漏洞得逞。测试设置使用 SDR——具体来说是 ADALM PLUTO——和一台笔记本电脑，但您可以很容易地想象出一个更小的包，用于秘密的步行式攻击。[Mordechai]还为撒旦提供了一个潜在的对策，它基本上是击败硬盘驱动器，产生射频噪声，以掩盖任何产生的信号。

虽然它的实际应用可能有限，但撒旦是一个有趣的旁道攻击来添加到[古里博士]的攻击列表中。从使用安全摄像头的[光学渗透](https://hackaday.com/2017/09/21/another-day-another-air-gap-breached/)到将电源变成扬声器的，漏洞不断增加。

 [https://www.youtube.com/embed/rlmP-csuFIo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/rlmP-csuFIo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[chuckt]的提示。

[通过[哔哔声计算机](https://www.bleepingcomputer.com/news/security/air-gapped-systems-leak-data-via-sata-cable-wifi-antennas/)