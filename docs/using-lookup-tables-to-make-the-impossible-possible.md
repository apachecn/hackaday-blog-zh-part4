# 使用查找表将不可能变为可能

> 原文：<https://hackaday.com/2020/01/10/using-lookup-tables-to-make-the-impossible-possible/>

尴尬的表白时间:我从没在小学学过乘法表。当然，我有像 2 和 5 这样的简单表格，但如果问我 4×7 或 8×6 是多少，我会答不上来。你可以想象，这使我成为一个不太优秀的数学学生，我在有时间限制的考试中特别有障碍，有很多长乘法问题。当你把这些表存入内存时，标准算法要快得多，我发现这让我很悲哀。

当我观看 [Charles Lohr 的 2019 年 Supercon 关于查找表](https://www.youtube.com/watch?v=LnqqvVp_UZg)或 lut 的有用性和灵活性以及它们简化甚至完全避免计算密集型操作的能力的演讲时，我想起了这段痛苦的记忆。当然，大多数 LUT 实现解决的问题比乘法表要复杂一些，但这不是必须的。正如查尔斯指出的那样，甚至用来填充参考书中一页又一页的正弦表和对数表都被移植到了硅片上，在硅片上根据用户输入查找正确答案要比通过计算得出答案容易得多。

[![](img/3f2f40304d66f740813e756dea8ed78b.png)](https://hackaday.com/wp-content/uploads/2019/12/CNLohr-minecraft-server-running-off-of-AVR.jpg)

Yes, this is a Minecraft server all thanks to LUTs.

lut 如何实现看似不可能的事情的一个最有趣的例子是在一个老项目中，Charles 试图在 atmega 168 上构建一个《我的世界》服务器。向客户端发送数据块(游戏世界的一部分的数据表示)是《我的世界》服务器的基本工作，并且在普通机器上涉及使用数据压缩。他没有尝试在 8 位微控制器上实现 zlib，而是转向了一个 LUT，它只是向客户端提供原始字节，而服务器根本不知道这些字节是什么意思。一些功率逆变器使用类似的技术，通过将一个完整周期的值从一个字节阵列馈送到 DAC 来合成正弦波输出。很暴力，但很管用。

另一个有趣且出乎意料的发现是 lut 不一定是软件。有些可以在完全机械的系统中实现。查尔斯用了轴上凸轮的例子；在汽车引擎中，这些代表了每个汽缸在正确的时间打开和关闭阀门所需的代码。更复杂的例子是曾经在舰炮火控计算机中发现的凸轮和齿轮，或者用于提花织机的程序卡。他甚至向 Wintergatan 大理石机脱帽致敬，它的大型编程鼓和钉子就像一个硬件 LUT。

我发现查尔斯的演讲内容广泛，引人入胜。最初我认为这将是一个关于 FPGA 的演讲，但他直到最后才真正谈到 FPGA 的具体内容。不过，结果还不错——光是听到 LUT 能解决的所有酷问题就值回票价了。

出于好奇，是的，我最终还是记住了乘法表。奇怪的是，只有在我开始玩数字并使用我的第一个计算器看到它们之间的关系后，我才明白，讽刺的是，它可能使用 lut 来计算结果。

 [https://www.youtube.com/embed/LnqqvVp_UZg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/LnqqvVp_UZg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

