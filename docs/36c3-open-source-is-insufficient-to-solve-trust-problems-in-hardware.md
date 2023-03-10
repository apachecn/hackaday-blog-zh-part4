# 36C3:开源不足以解决硬件中的信任问题

> 原文：<https://hackaday.com/2019/12/29/36c3-open-source-is-insufficient-to-solve-trust-problems-in-hardware/>

有了开源软件，我们已经习惯了某种程度的信任，无论我们在电脑上运行什么，都是我们所期望的。由于开发和部署周期中各个部分的散列和公钥签名，第三方很难在我们不容易发现的情况下修改源代码或可执行文件，即使它通过不可信的渠道传播。

不幸的是，当谈到开源硬件时，在我们拥有最终产品之前，我们无法控制的步骤和参与方的数量——生产、物流、分销，甚至客户——使得实现同样的安心变得更加困难。更糟糕的是，要真正验证芯片级的硬件，你最终必须摧毁它。

在他今年在 36C3 的演讲中，[bunnie]展示了我们在制造过程中可能面临的几种攻击媒介的详细见解。跳过添加或替换元件等显而易见的问题，他专注于具有引线键合或硅通孔(TSV)植入的 IC 封装内雄心勃勃且难以检测的修改，下至修改集成电路本身的网表或掩模。这些不是任何理论上的或“如果”的情景，而是实际可能的选择——当然，其中一些有一定的价格标签，但最终，有了正确的动机，钱只是一个细节。

当然，对于一个闪烁的 LED 项目来说，这些都不是特别可行，甚至没有多少兴趣，但是考虑到越来越多的开源硬件项目如何取代完全专有的组件，尤其是在主要关注隐私的情况下，至少可以说，在这个过程中对所涉及的硬件缺乏信任肯定是令人担忧的。在这一点上，没有完美的解决方案，但 FPGAs 可能是下一个最好的东西，演讲的下一部分是展示[bunnie]与[xobs]和[Tom Marble]一起工作的[be trusted](https://betrusted.io/)原型。在我们看来，仅此一点就让这场演讲值得一看。

 [https://www.youtube.com/embed/Hzb37RyagCQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Hzb37RyagCQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

