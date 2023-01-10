# 世界是你的绿屏

> 原文：<https://hackaday.com/2020/12/22/the-world-is-your-green-screen/>

今年是家庭视频会议年。如果你真的很能干，你已经设法装上了某种绿色屏风，这样你就可以隐藏你的混乱，看起来好像你在你的上东区的豪华办公室里。然而，大多数消费者视频会议现在有一些方法来尝试猜测你的背景是什么，并在没有绿屏的情况下替换它。然而，结果往往不尽如人意。最近华盛顿大学[的一篇论文](https://arxiv.org/pdf/2012.07810.pdf)概述了一种使用机器学习的新的[背景抠图程序](https://grail.cs.washington.edu/projects/background-matting-v2/)，正如你在下面的视频中看到的，结果相当不错。在 [GitHub](https://github.com/PeterL1n/BackgroundMattingV2) 上有代码，甚至还有基于 Linux 的[网络摄像头](https://github.com/andreyryabtsev/BGMv2-webcam-plugin-linux)过滤器。

该算法确实需要一个没有你的背景镜头，我们想象这需要相对静态。从观看视频来看，似乎这种软件的酸性测试是 spiky hair。有几个绝对不是秃顶的人使用这种方法和其他背景替代品(如 Zoom 中的一个)翻转头发的比较。

结果的质量在一定程度上取决于过滤器可以处理多少像素，因此 4K 视频似乎比低分辨率的效果更好。尽管如此，它并不完美，但看起来确实比一些现有的工具做得更好。如果你自己尝试，我们确实读到过你想避免阻挡强光，尤其是在背景拍摄时，并尽量保持光照恒定。对于长时间使用，随着光线条件的变化，重新拍摄背景图像可能会有所帮助。

正如你所料，你需要一个大显卡来实时完成这项工作。这是事实，因为该算法似乎与 4K 输入更好地工作。不过如果你是做后期视频制作的，大概可以用硬件换时间。

我们已经在 DeepBackSub 上看到了类似的努力。一旦你有了这个工作，你可以建立一个[镜](https://hackaday.com/2020/05/29/two-way-mirror-improves-video-conferencing/)来改善你的视频会议眼神交流。

 [https://www.youtube.com/embed/b7ps21MVyTA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/b7ps21MVyTA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

