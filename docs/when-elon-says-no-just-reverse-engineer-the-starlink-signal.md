# 当[埃隆]说不的时候，就反向工程 Starlink 信号

> 原文：<https://hackaday.com/2022/10/22/when-elon-says-no-just-reverse-engineer-the-starlink-signal/>

我们都知道，有时请求原谅比请求允许做某事更好，我们大胆猜测，我们中的许多人有时会把这个建议放在心上。但是[托德·汉弗莱斯]试图利用 Starlink 网络作为全球定位系统的备份，结果把操作顺序搞混了，最后做了一些有趣的逆向工程工作。

据说[Todd]和他在德克萨斯大学奥斯汀分校无线电导航实验室的团队，代表他们在美国陆军的赞助商，与 Starlink 接触，讨论合作一个项目，使他们的低地球轨道星座提供定位、导航和定时功能。虽然最初对这个项目感兴趣，但 Starlink 的负责人[Elon Musk]阻止了事情的发展，让[Todd]的团队陷入困境。不听劝阻，他们买了一个 Starlink 用户终端，建造了一个相当于小型射电望远镜的东西——尽管我们已经看到[只用一个 RTL-SDR](https://hackaday.com/2022/09/23/snooping-on-starlink-with-an-rtl-sdr/) 做了类似的事情——并开始逆向工程 Starlink 的 Ku 波段下行链路信号的结构。关于他们发现的[论文](https://radionavlab.ae.utexas.edu/wp-content/uploads/2022/10/starlink-structure.pdf) (PDF 链接)充斥着大量细节，例如 Starlink 使用正交频分复用(OFDM)方案。

值得注意的是，他们的目标不是破解加密或窥探用户数据；相反，他们想要访问 Starlink 数据结构中嵌入的同步和定时信号。通过使用这些数据以及公开可用的每颗卫星的星历表，可以快速计算到多颗卫星的准确距离，并确定接收器的位置，误差在 30 米以内。它不如我们见过的一些 GPS-Starlink hacks 好，但在紧要关头仍然相当不错。此外，这里的逆向工程工作非常值得一读。

感谢[阿德里安]的提示！