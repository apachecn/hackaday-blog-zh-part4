# 无校准金属探测器

> 原文：<https://hackaday.com/2022/07/17/a-no-calibration-metal-detector/>

多年来，发现对电子产品热爱的人的一个传统早期项目是金属探测器。这在过去意味着几个晶体管，但今天更有可能涉及微控制器。[Mircemk]有一个用单晶体管振荡器和 Arduino 弯曲两个世界的例子。

这种金属探测器有一个大的搜索线圈，它是振荡器调谐电路的一部分。当一块金属进入它的范围时，振荡频率就会改变。在过去，这可能是用另一个振荡器检测到的音频拍频。这种设计需要在检测开始时进行校准，将两个振荡器调谐到相同的频率。

该检测器保留第一个振荡器，但避开第二个振荡器，支持 Arduino。微控制器充当频率计数器，监控频率并在检测到可能由一块金属引起的变化时发出警报。它可能没有人耳在全模拟时代应用于拍频的一些精细度，但它足够简单，可以避免校准的需要。看到它在下面的视频休息，我们相信，就像那些晶体管模型旧，将有很多乐趣。

Arduino 可能是目前的热门产品之一，但它会取代 555 吗？[也许在金属探测器的世界里没有](https://hackaday.com/2021/08/30/impromptu-metal-detector-built-from-the-junk-bin/)！

 [https://www.youtube.com/embed/mFrAF6r_HkQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/mFrAF6r_HkQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

