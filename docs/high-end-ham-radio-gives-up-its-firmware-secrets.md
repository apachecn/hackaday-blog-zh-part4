# 高端业余无线电放弃其固件秘密

> 原文：<https://hackaday.com/2020/07/14/high-end-ham-radio-gives-up-its-firmware-secrets/>

业余无线电操作员一直在他们的游戏中处于领先地位，当他们一直在黑无线电的时候。一个业余无线电爱好者许可证允许你打开一台收音机并修改它，或者甚至从头开始建造一台收音机。诚然，随着技术的进步，老派无线电黑客的机会已经减少，但这并不意味着新的电脑化无线电不会受到勤奋的哈姆的温柔服务。

一个典型的例子:[建伍 TH-D74A 的固件已经被转储并部分解码](https://kk4vcz.com/posts/th-d74-firmware/)。[Hash (AG5OW)]和[Travis Goodspeed (KK4VCZ)]之间有点非正式的合作，这个过程始于[Hash]拆除他的收音机，见下面的视频。收音机是一种三频便携式对讲机，功能远超最复杂的廉价进口，价格也与之匹配，有一个串行端口和 JTAG 连接器。一个 JTAGulator 允许他探索一些秘密，但完整的探索需要花费 140 美元为无线电购买一个备用 PCB，并需要一些灵巧的工作来移除 BGA 封装的闪存 ROM 并将其映像转储到磁盘。

[特拉维斯]从那里拿起分析。他在图像中发现了三个程序，包括收音机的固件和收音机用户界面中使用的一串字符串，有英语和日语版本。这项工作还远未完成，但是已经有了进一步探索和潜在的未来固件补丁的基础，以便为无线电提供不同的功能集。

这是逆向工程中一个很好的案例研究，真的值得深入了解更多。如果你正在寻找一个更正式的逆向工程探索，你可以做得比刚刚结束的 [HackadayU 的“用 Ghidra 进行逆向工程”课程](https://hackaday.io/project/172292-introduction-to-reverse-engineering-with-ghidra)差得多。请尽快观看课堂视频。

 [https://www.youtube.com/embed/Q_n_bs6f8gE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Q_n_bs6f8gE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

