# 无人机对无人机战，带干扰器

> 原文：<https://hackaday.com/2019/07/24/drone-on-drone-warfare-with-jammers/>

在 2018 年伦敦盖特威克机场涉嫌无人机袭击事件后，我们一直在寻找针对这些流氓无人机操作员的有效对策。土耳其的[Ogün Levent]创造了一个有趣的解决方案，并在他的 Dronesense 页面上简要记录了这个解决方案。由于保密协议的原因，文章中有一些空白，但我们很可能会对缺失的内容做出一些很好的猜测。

不是一个，而是两个石灰被发送到定制无人机上的空中，以追踪其他无人机，并通过干扰它们的信号来击倒它们，这通常比试图向它们发射空对空导弹安全得多！

![](img/e49d88df25e9cf0c5249def6ab543d24.png)【ogün Levent】和他的团队使用的无人机硬件是定制的 S600 框架，带有 T-Motor U3 电机和 40 A 速度控制器，起飞重量为 5 kg。一台 [Adventech 单板计算机](https://www.advantech.com/products/35-single-board-computers/sub_1-2jkj91)是主控制器，带有一个 Pixhawk 次级，最重要的是，一个 4 W，2.4 GHz 频率的干扰器，射程为 1200 米。

派遣一架带有反措施的猎人无人机而不是试图在地面上进行反措施的一大优势是，距离无人机更近，干扰机的功率可以降低，从而对该地区的其他射频设备产生更少的干扰——流氓无人机是专门针对的。

其中一个 LimeSDRs 运行 GNU 无线电流程图，其中有一个专门设计的模块，用于检测流氓无人机的调频信号，这似乎是一个机器学习分类脚本。另一个 LimeSDR 运行另一个*secret*流程图，在 SBC 上运行的自定义脚本将两个流程图结合在一起。

现在是有趣的部分，第二个 LimeSDR 是做什么的？整体概念的一些更明显的问题是，无人机会干扰自己，流氓无人机可能已经安装了抗干扰能力，在这种情况下，它只会返回家中。也许第二个 SDR 是为了在无人机回家时跟踪它，从而抓住人类操作员？下面评论里的回答/建议！休息后的视频。

 [https://www.youtube.com/embed/R-0hRMLxVIE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent&listType=playlist&list=UUrhC6scFdHoQM8R6jv4N8UA](https://www.youtube.com/embed/R-0hRMLxVIE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent&listType=playlist&list=UUrhC6scFdHoQM8R6jv4N8UA)



我们自己的 Jenny List 报道了盖特威克无人机目击事件的一些细节:[伦敦盖特威克机场因无人机目击事件关闭了大门](https://hackaday.com/2018/12/20/london-gatwick-airport-shuts-its-doors-due-to-drone-sighting/)和[揭露了无人机对飞机的歇斯底里。](https://hackaday.com/2016/05/02/debunking-the-drone-versus-plane-hysteria/)