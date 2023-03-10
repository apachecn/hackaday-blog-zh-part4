# 堪萨斯城式 6502 试验板计算机的盒式接口

> 原文：<https://hackaday.com/2022/10/11/a-cassette-interface-for-a-6502-breadboard-computer-kansas-city-style/>

计算机爱好者把他们的程序和数据储存在盒式磁带上已经有很长时间了。但是因为软驱是昂贵的外围设备，而硬盘离成为今天的商品还有很长的路要走，盒式磁带在大容量数据存储堆的顶端享受了很长一段时间。

通过探索盒式数据存储技术来庆祝这一成功是[【Greg Strike】的堪萨斯城解码器项目](https://www.gregorystrike.com/2022/10/01/kansas-city-standard-decoder/)背后的想法，他希望将其用于他的[【食本者】](https://eater.net/)型 6502 计算机。下面的视频解释了堪萨斯城标准的一些细节，并包括一些有趣的历史背景，我们真的没有深入研究过。关于 KCS 使用的调制方案，也有一些很好的技术细节，这是[Greg]用来构建的基础。在一次使用 LM567 音频解码器芯片的失败尝试后，他偶然发现了[【麦森】的 KCSViewer 项目](https://hackaday.com/2018/10/07/reading-old-data-tapes-the-hard-way/)，该项目只用分立元件就能解码 KCS 编码的音频信号。

[Greg]的原型有一个将正弦波转换为方波的比较器，后面是一对单稳态定时器，每个定时器都被调谐到 KCS 规格中定义的高频或低频。使用 Audacity 创建的测试信号——有什么是它做不到的吗？—成功解码，为项目的第一阶段提供了概念证明。我们期待着该系列的其余部分，这将把它变成一个实际的解码器，可能还会添加一个编码器。

收听[黑客日播客](https://hackaday.com/podcasts/)的听众可能还记得，几个月前我们曾尝试使用 [KCS 在一集](https://hackaday.com/2022/07/01/unraveling-the-hackaday-podcast-hidden-message/)中隐藏一些数据。

 [https://www.youtube.com/embed/6m7vDhscGzU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/6m7vDhscGzU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

