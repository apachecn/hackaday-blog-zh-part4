# 将 80 年代的打字机转换成 Linux 终端

> 原文：<https://hackaday.com/2022/08/04/converting-an-80s-typewriter-into-a-linux-terminal/>

打字机的全盛时期可能早已过去，但仅仅因为个人电脑、文字处理软件和廉价打印机已经使它们基本过时，并不意味着没有它们世界会更好。使用打字机是一种丰富的感官体验，从你手指下按键的感觉，甚至是最响亮的 PC 键盘都无法与之相比，到打字时奇怪的普遍声音。

所以，如果生活给了你一台打字机，为什么不把它重新投入工作呢？这正是[Artillect]通过将一台 80 年代的打字机转换成 Linux 终端所做的。这台打字机是 AX-25 的兄弟，是一种先于文字处理软件的电子打字机，有一个菊花轮打印头，一个小液晶显示器，和一个巨大的 8k 内存用于编辑文件。[Artillect]首先计算出打字机的 8×11 矩阵中哪些键对应哪些字符，然后转动一个 Arduino 和两个多路复用器来驱动打印头。打字机的键盘还用于输入，因为该项目仍然处于原型阶段，所以 Raspberry Pi 充当了打字机和笔记本电脑之间的串行监视器。下面的视频很好地概述了布线和软件，并显示了打字机敲打出 Linux 命令行输出。

目前，[Artillect]的打字机基本上就像是老式的电传打字机。有足够的空间进一步发展；例如，我们希望看到它变成一个内置打印机的网络平台。但即使只是作为一个概念的证明，这也很棒，你可以肯定我们会在旧货店和旧货市场寻找旧打字机。

 [https://www.youtube.com/embed/JvhT_Bru0AA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/JvhT_Bru0AA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

