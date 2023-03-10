# 这是圆周率所有的方式与这个圆周率供电采摘机器人

> 原文：<https://hackaday.com/2022/09/20/its-pi-all-the-way-down-with-this-pi-powered-pi-picking-robot/>

虽然我们大多数人生活在一个曾经无处不在的树莓派现在像母鸡的牙齿一样罕见的世界，但有一个神奇的地方，他们有如此多的派，以至于他们需要建造一个机器人分配器来挑选派订单。雪上加霜的是，他们甚至用树莓派制造了这台神奇的机器。恐怖。

这个神奇的地方？当然是澳大利亚。上面链接的 Pi Australia 的文章没有公布日期，但它确实提到有一台 Pi 4 Model B 在运行该节目，所以这至少是最近的事。原料储存在一排倾斜的箱子中，穿梭机构通过 X-Y 门架进入这些箱子。航天飞机停靠在一个垃圾箱前，用一个步进器控制的手指翻转一个盒子，将它们放在垃圾箱里。一旦进入梭子，订单就被运送到一系列输出箱，在那里，伺服操作挡板将产品毫不客气地倾倒出来，以便包装和运输。下面有一个完整周期的视频，但有一个警告——X-Y 机架上的步进电机真的会尖叫，所以你可能需要降低音量。

这篇文章不仅更详细地介绍了“主教”的建造——以*外星人*中的英雄合成生物命名——还介绍了建造过程中面临的挑战。事实证明，即使你试图用重力来简化这样的系统，事情也很容易出错。关于软件也有相当多的细节，令人惊讶的是围绕 LinuxCNC。而且有计划要更进一步，用另一个机器人来做订单的包装、密封和贴标签。如果他们需要下面所有的自动化，我们想我们找到了所有丢失的 pi。

[https://player.vimeo.com/video/749777452?h=3b81c96ac8&dnt=1&app_id=122963](https://player.vimeo.com/video/749777452?h=3b81c96ac8&dnt=1&app_id=122963)

感谢[尼克欧文]的提示。