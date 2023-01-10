# PineTime 智能手表和好代码玩坏苹果

> 原文：<https://hackaday.com/2021/10/16/pinetime-smartwatch-and-good-code-play-bad-apple/>

PineTime 是 Pine64 的朋友送的开放式智能手表。[TT-392]想要证明硬件可以播放全动态音乐视频，在某种程度上，他们是正确的。当你看下面的视频时，你应该注意到单色动画保持着健康的帧速率，这是所有努力的结果。在没有任何修改的情况下，视频最高可以达到大约每秒八帧。

要转换一个 MP4，你需要把它分解成图像，这样可以去掉声音。接下来，你将它们加载到 Linux 专用的视频处理器中，该处理器会寻找需要改变的像素簇，并忽略静态像素。相关像素选择减轻了运行到显示器的数据的负担，提高了 fps，因为您不必浪费时间提醒它黑色像素块应该保持原样。最后，该过程将压缩所有内容，以适应手表的板载内存。尽管这是几分钟的黑白图片，但编译可能需要几个小时。

你将需要访问手表的内部，所以希望你有开发工具包或不介意破解密封。我们在骗谁，你不是为了完整的保修而来的。视频驻留在闪存芯片中，您必须一次传输一个块。坏苹果需要十四个，所以你可能想在一个较短的视频上练习。最后，核心内存需要一些更新才能正常播放。现在你可以坐下来…看着。

Pine64 在单板计算机方面起步艰难，但他们正在通过诸如烙铁和无谷歌的 T2 Linux 手机赢得我们的信任。

 [https://www.youtube.com/embed/RqL8V3xWmxg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/RqL8V3xWmxg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

