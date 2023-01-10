# VHS 解码项目有助于档案工作

> 原文：<https://hackaday.com/2022/12/13/vhs-decode-project-could-help-archival-efforts/>

从旧存储介质归档数据可能是一个非常复杂的过程。它可以像把磁盘放入旧驱动器并读出内容一样简单。然而，如今的技术水平更加复杂，先进的技术有助于恢复尽可能多的数据。VHS-Decode 项目旨在改善旧模拟录像带的存档。

该项目是由[查德·佩奇]于 2013 年开始的以激光视盘为中心的 [ld-decode](https://github.com/happycube/ld-decode) 的一个分支，读者可能还记得它曾被用于《末日审判》复制器——一种旨在从 BBC 古老的《末日审判》激光视盘中恢复数据的设备。VHS-Decode 旨在直接从磁带磁头中捕获原始 RF 信号，这是物理介质上信号的最直接表示。从那里，这些信号可以以各种方式处理，以最好地恢复原始音频和视频轨道。这和软盘恢复工具使用的技术差不多，比如 T4 的 flux engine T5。

尽管有 VHS 的名字，代码目前可以与几种磁带格式一起工作。VHS、S-VHS 和 U-Matic 支持 PAL 和 NTSC 格式，而 Betamax、Video8 和 High8 磁带采集仍在进行中。使用该代码需要一个带有测试点或迹线的录像带播放器，以使来自头部的信号可被访问。捕捉这些信号是通过末日复制器硬件设备或 Conexant CX2388x 模数转换器实现的，这种转换器通常出现在许多旧的 PCI 电视调谐器卡中。然后可以使用各种技术将捕捉到的信号转换成可观看的视频文件。

我们喜欢一个好的档案项目，VHS-Decode 显然是抢救旧录像带的有用工具。

 [https://www.youtube.com/embed/L08zpYg7Ssg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent&listType=playlist&list=PL1oumm4MF81s3gpchCyBM8z9DWe3K82mq](https://www.youtube.com/embed/L08zpYg7Ssg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent&listType=playlist&list=PL1oumm4MF81s3gpchCyBM8z9DWe3K82mq)



【感谢 JohnU 的提示！]