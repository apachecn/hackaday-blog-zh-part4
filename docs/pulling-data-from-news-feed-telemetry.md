# 从新闻传送遥测中提取数据

> 原文：<https://hackaday.com/2020/05/31/pulling-data-from-news-feed-telemetry/>

我们习惯于每天从电视新闻直升机上看到镜头，它们是 21 世纪生活背景的一部分。但我们经常听到他们被录音室评论覆盖，所以听到他们的原始音频包含遥测技术是很有趣的。这引起了[proto17]的注意，他们从新闻直升机视频[中提取了一些音频，并对其进行了彻底的调查，以检索数据](https://github.com/proto17/HelicopterDemod/wiki)。

这篇文章非常深入，虽然承认有些步骤可以用现成的工具更容易地执行，但它的要点是在较低的层次上完成所有步骤。因此，这种行为主要发生在 GNU Radio 中，我们看到了识别信号并将其频率下移，然后推断其波特率以检索其内容的过程。不过故事还没有结束，因为在最终检索数据本身之前，我们会深入研究一些 ASCII 技巧来识别数据包帧。它仍然没有告诉你数据包含什么，但这是一个迷人的过程。

人们很容易忘记 GNU Radio 的信号处理能力远远超出了无线电，但是[它是一个迷人的超级会议演讲](https://hackaday.com/2020/02/21/software-defined-everything-with-mike-ossmann-and-kate-temkin/)的主题。我们甚至在今年愚人节的中加入了[的非愚蠢部分。](https://hackaday.com/2020/04/01/gold-cables-really-do-work-the-best/)