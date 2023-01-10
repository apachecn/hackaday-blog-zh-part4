# 哟伙计，我们听说你喜欢复古电脑

> 原文：<https://hackaday.com/2021/08/14/yo-dawg-we-heard-you-like-retrocomputers/>

让软件翻译程序在你 3000 美元的游戏电脑上模拟超级任天堂，或者更实际地，在新的 M1 Mac 电脑上运行 x86 软件，这种想法似乎很现代，因为它在当今的计算机世界如此普遍。像这样使用软件的想法实际上要古老得多，很容易追溯到 80 年代的 Commodore 和 Atari 个人电脑时代。他们的硬件实际上没有太大的不同，只要有一点耐心和专业知识，就有可能在 Atari 上编译 Commodore 64 内核，但有一些限制。

这个项目来自[un bium ],灵感来自他最近看到的一个视频，在这个视频中，最初的苹果电脑在 Commodore 64 上被模拟。不过，他在这个建筑中采用了不同的方向。第一步是重新格式化 C64 代码，以便它可以在 Atari 上编译，这主要是通过 Python 脚本和一些手动调整来完成的。从那时起，他开始确保 rom 能够真正运行。这两台机器的内存设置非常相似，这使得这稍微容易一些，但他需要一些变通办法来解决一些减速带。最后，光标和 HMI 被配置好，一旦其他一些事情被理顺，他就有了一个在 8 位 Atari 上运行 C64 软件的工作系统。

不出所料，有一些事情是行不通的。除了键盘和鼠标之外没有 IO，保存和加载程序还不可能。然而，【unbibium】已经将他的所有代码放在他的 [GitHub 页面](https://github.com/unbibium/atari64)上，如果有人想扩展他的工作，也可以在未来的版本中改进这个项目。但是，如果您正在寻找一个更容易的入口点来模拟现代的 Commodore 软件，有一个项目可以从 Raspberry Pi 运行 C64。

感谢[Cprossu]的提示！