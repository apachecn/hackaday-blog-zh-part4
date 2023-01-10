# 合作努力让激光电流计说出 g 代码

> 原文：<https://hackaday.com/2022/07/15/collaborative-effort-gets-laser-galvos-talking-g-code/>

现在每个人都应该知道，当项目取得进展时，我们喜欢跟进。能够庆祝成就并看到一个项目是如何随着时间的推移而改变的，这是一件很棒的事情。但是突出一个不仅进步，而且对社区有一点回馈的项目是特别棒的。

这就是我们看到的[【Les Wright】用二手激光雕刻机](https://hackaday.io/project/186320-laser-coder-repaired-and-hacked)继续工作的情况。就在几周前，我们特别报道了[用易贝 find 进行的初步实验](https://hackaday.com/2022/06/11/inside-an-ebay-marking-laser/)，这是一种最初用于工业标记应用的强大 CO [2] 激光器。起初看起来[Les]不得不满足于一个漂亮的拆卸和收获几个零件，但 11 岁的电子管和打标头的电流计实际上工作得很好。

目前的工作，也是下面视频中的特色，主要涉及这些 galvos，特别是让他们与 g 代码一起工作，将该单元变成一个特设的激光雕刻机。幸运的是，他在 GitHub 上偶然发现了 [OPAL Open Galvo 项目](https://github.com/opengalvo/OPAL)，它可以将 g 代码转化为他的激光器使用的 XY2-100 协议。虽然[Les]对 OPAL 的软件方面赞不绝口，但他看到了一个他可以填补的硬件漏洞，并贡献了他的 PCB 设计，该 PCB 包含代码运行所需的 Teensy 以及运行检流计和激光器所需的缓冲器和线路驱动器。视频展示了在木材和丙烯酸上使用简单设计的整个过程，以及在玻璃上的有趣结果。

当然，这些只是测试——我们确信[Les]将在更完整的雕刻机中解决明显的安全问题。但是现在，我们只是为这里展示的合作鼓掌，并等待更多的更新。

 [https://www.youtube.com/embed/w4mWgVDPIiQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/w4mWgVDPIiQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

