# 当一家自行车共享初创公司倒闭时，你会怎么处理这些自行车？

> 原文：<https://hackaday.com/2020/06/03/when-a-bike-sharing-startup-goes-away-what-do-you-do-with-the-bikes/>

过去几年，许多城市的一部分垃圾是无处不在的自行车和滑板车，这些公司通过智能手机应用程序提供按小时出租的服务。当它们被使用者随意丢在人行道上时，它们会让人很讨厌，有时它们的数量会比骑车人多很多倍。2018 年，对于中国以外的许多城市来说，它们的数量变得不那么多了，因为中国自行车共享服务 Ofo 收缩了业务，并从街上撤走了其独特的黄色机器。几年后，那些被出售或被公司遗弃的 Ofo 自行车仍然存在。如果他们的锁被拆除，他们可以使用，但这样做是忽视了锁的潜力。[Aladds] [为 Ofo 锁编写了一个固件，允许通过在按钮](https://github.com/aladds/OFO_Lock)上输入代码来解锁。

锁上有一个 nRF51822，4G 无线电，当然还有锁机制本身。电池现在可能已经没电了，尽管他没有告诉我们是什么，但值得我们指出的是，类似的设计有时会使用危险的 LiSOCl2 化学物质，任何黑客都应该非常小心。他给了我们寻找芯片编程连接的完整说明，可以下载其现有固件进行检查，也可以删除固件以插入新版本。为了展示代码的运行，我们还在视频下方放了一个 YouTube 视频短片。与此同时，在 2018 年之前，我们已经窥视过 Ofo 锁的内部。

 [https://www.youtube.com/embed/dOF5OYbdcFc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/dOF5OYbdcFc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



Ofo 单车图片:Popolon / [CC BY-SA 4.0](https://commons.wikimedia.org/wiki/File:Ofo_bicycle_in_Paris.jpg)