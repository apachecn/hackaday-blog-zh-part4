# 一家公司如何破解 GameCube 光盘保护

> 原文：<https://hackaday.com/2019/02/04/how-one-company-cracked-the-gamecube-disc-protection/>

任天堂 GameCube 是 Big N 的第一款基于光盘媒体的游戏机。制造成本高得离谱的墨盒不见了。理论上来说，游戏可能会更便宜(是的，没错)，而且会有更多的纹理、图片和视频。大约在 GameCube 上架的时候，你的基本家用电脑开始有 DVD 刻录机，你可以走进电路城买那些小小的 DVD-r。但是你做不到。你不能烧 GameCube 游戏，至少没有先进的焊接技术。

一家公司做到了。制作动作回放的英国公司 datel,“GameCube 的游戏精灵”想出了如何绕过 Game cube 的光盘保护。不仅如此，自从动作回放进入市场以来的 15 年里，没有人能够复制他们的方法。在一个迷人的视频中，[Nathan] [带我们参观光盘，看看这种光盘保护方案实际上是如何工作的](https://www.youtube.com/watch?v=3l1XacYh25g&feature=youtu.be)，以及如何利用它从 SD 卡加载自制游戏。

任天堂 GameCube 光盘格式几乎(但不完全)与 DVD 格式相同。在(几乎)每张 DVD 和几乎每张 GameCube 光盘上，光轨内部都有一个各种各样的“条形码”。[这个突发剪切区域](https://en.wikipedia.org/wiki/Burst_cutting_area) (BCA)对于从单个母版上生成的每个副本都是唯一的。此外，这种 BCA 只能用比 DVD 刻录机中的激光二极管功率大得多的 YAG 激光器切割。

但是 Datel 的动作回放盘没有这个 BCA。为什么不呢？[BCA 有效地覆盖了 DVD 中第一个数据块的凹坑和平台](https://debugmo.de/2008/11/anatomy-of-an-optical-medium-authentication/)。由于 BCA 覆盖了已经存在的数据，您可以将 BCA 应该保存的任何数据编码到坑和脊的原始数据中。这是一项卓越的技术，它允许消费设备制作动作回放光盘。但令人惊讶的是，这种技术并没有在 GameCube 家酿场景中普及。

不管怎样，这并不重要；有了 modchips，有了 SD 到存储卡的适配器，你就可以运行自制软件，而不必刻录光盘。这正是[Nathan]在他的 GameCube 设置中所做的，你可以看看下面的视频。

 [https://www.youtube.com/embed/3l1XacYh25g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/3l1XacYh25g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

