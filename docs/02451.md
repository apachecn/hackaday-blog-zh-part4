# Octavo 系统公司展示了死 bug Linux 计算机

> 原文：<https://hackaday.com/2019/03/15/octavo-systems-shows-off-with-deadbug-linux-computer/>

曾几何时，支持 Linux 的小型单板计算机还是新奇事物，但现在不是了。今天，我们有很多选择，很多都是围绕我们可以为自己的项目购买的模块构建的。这些主板背后的一些芯片组供应商在成本上进行竞争，其他供应商找到了一个利基来区分他们的产品。Octavo Systems 是后者之一，它提供系统级封装(SiP)模块，专为易于集成而设计。他们描述了使用他们的 SC335x C-SiP 构建一台最小的计算机是多么简单，并且为了证明这一点，他们在 2019 年的嵌入式世界上带来了一个 deadbug 实现。【休息后的短视频。]

我们大多数人都会遇到八开模块[作为猎兔犬板](https://hackaday.com/2016/05/10/new-part-day-a-beaglebone-on-a-chip/)的心脏。它们的日益融合使得像[袖珍猎犬](https://hackaday.com/2017/09/23/the-tiny-25-pocketbone/)这样的小奇观成为可能。但是要使用所有这些引脚仍然需要一个四层电路板。Octavo 对硬件专业人员的推介集中在如何通过简单的集成节省时间来加快上市速度，幸运的是，对我们来说，简单的集成也转化为我们项目的更易访问的设备。发布一份文档描述一个假设的 Octavo 模块单层 PCB 是一回事，在没有 PCB 的情况下展示这一概念是另一回事。

当然，这个小机器只能使用模块的一小部分功能，如果目标只是让几个 led 闪烁，那就太夸张了。如果是这样，我们就用 555 个定时器！但它确实展示了一个简单的“Hello World”机器可以被构建成什么样，消除了恐吓因素并邀请更多的人来玩。

在我们的电路雕塑比赛中，前三名获奖者之一是一台线框 Z80 计算机。从 Z80 到 Octavo SC335x 有很大的飞跃，但我们已经看到了[扎克] [在 Supercon 2018 周末](https://youtu.be/WCLlz_taeQk?t=773)做出的一项努力，即建造一台带有 Octavo 模块的死 bug 计算机。用不了多久，就会有人用更复杂的东西超越这种极简主义的 LED 闪光灯，我们迫不及待地想看到它。

> 厉害了死 bug Linux 电脑由[的](https://twitter.com/octavosystems?ref_src=twsrc%5Etfw)[@ Welsh _ owl](https://twitter.com/welsh_owl?ref_src=twsrc%5Etfw)@ octavo systems 在 [@embedded_world](https://twitter.com/embedded_world?ref_src=twsrc%5Etfw) 在 3A 馆！pic.twitter.com/xOd3HlMNeF✨[# ew19](https://twitter.com/hashtag/ew19?src=hash&ref_src=twsrc%5Etfw)
> 
> —德鲁·富斯蒂尼(@ PDP 7)[2019 年 2 月 26 日](https://twitter.com/pdp7/status/1100349116515827712?ref_src=twsrc%5Etfw)