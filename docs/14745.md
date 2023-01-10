# 用传统的方式自举

> 原文：<https://hackaday.com/2022/09/09/bootstrapping-the-old-fashioned-way/>

PDP-11、Altair 8800 和 IMSAI 8080 是计算机革命的一些英雄，它们有一些共同点——前面板开关，并且有很多这样的开关。你可能对这些开关有一个模糊的概念，可能是从阅读 Levy 的《黑客》中得到的，那里简要描述了程序切换的痛苦过程。但是它到底是如何工作的呢？感谢戴夫车库的[戴夫·普卢默]，现在我们有了一个方便的教程。有问题的这台计算机是 IMSAI 8080 的复制品，这是一台因年轻的马修·布罗德里克在军事游戏中出名的计算机。【戴夫】[设法给复制品打分](https://www.youtube.com/watch?v=RdTMB4BHRMo)，一名观众帮他节省了组装时间。

示例程序是 Larson 扫描仪，也就是让一条光推动一个光脉冲穿过这条光。[Dave]从汇编代码开始，不到 11 行，然后通过一个可在线获得的汇编程序运行它。这给了我们机器码，但没有十六进制键盘输入，所以我们需要 8 位二进制字节。为了对机器进行实际编程，你将地址开关设置到你的程序开始位置，数据开关设置到你的第一个字节。“存放”开关设置该字节，而“存放下一个”开关递增地址，然后存储该值。这意味着你不必为每条指令输入地址，只需输入数据即可。到达程序的结尾，确认地址设置为开始，然后轻击 run。希望你把一切都切换正确。如果是这样，你会得到一个友好的扫描仪，让人想起 80 年代的电视节目。休息后留下来看演示！

 [https://www.youtube.com/embed/DM4rZZBqXVM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/DM4rZZBqXVM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

