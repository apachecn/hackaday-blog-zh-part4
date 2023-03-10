# C#，适用于所有平台的语言–现在包括 Windows 3.11 和 DOS

> 原文：<https://hackaday.com/2020/02/09/c-the-language-for-all-platforms-now-including-windows-3-11-and-dos/>

微软。自千禧年以来，NET framework 就以这样或那样的形式伴随着我们，尽管它在很大程度上仍然是微软世界的领地，但从那时起，它已经通过各种实现进入了其他平台，包括 MacOS 和 GNU/Linux。就微软而言，尽管其历史只能追溯到 Windows 98，但更早的微软操作系统仍是禁区。

只是一点点。NET 在 DOS 和 Windows 3.11 中的运行得到了[Michal strehovsk]的支持。Windows 3.11 和 DOS 的 net C#代码。一个深入的解释[来自【斯科特·汉瑟曼】](https://www.hanselman.com/blog/NETEverywhereApparentlyAlsoMeansWindows311AndDOS.aspx)，它涉及了一些自 20 世纪 90 年代初以来跨越几十年的技巧。的。NET Core compiler 的目标文件可以输入到微软 C++编译器的旧版本附带的链接器中，当与微软的 Win32s 兼容层(将一些 Windos NT 的 API 引入 16 位操作系统)一起使用时，可以让 2020 年的 C#运行起来就像是回到了 1992 年。同时，DOS 版本使用。NET Core 生成自包含可执行文件的能力，以及一些非常重要的技巧，将最终程序的大小从几兆字节缩减到最终适合 DOS 的 27k 字节。还记得比尔·盖茨的名言吗，即“ *640k 对任何人来说都应该足够了*，这是指在没有额外内存扩展技巧的情况下，DOS 可用的最大*内存。*

这两个软件都不是特别有用，我们也看不到 C#程序员涌向这些新平台。但是我们为他的独创性喝彩，让旧的硬件做新的花样是我们的拿手好戏。这无疑勾起了我们过去的一些回忆。与此同时我们还特别介绍了。NET 在过去几年的几个项目中，[最近在 FPGA 上](https://hackaday.com/2019/12/15/net-to-fpga-with-hastlayer/)。