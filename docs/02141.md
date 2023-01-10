# DAT，我们从来不知道我们拥有的高清录像带格式

> 原文：<https://hackaday.com/2019/02/24/dat-the-hd-video-tape-format-we-never-knew-we-had/>

当我们通过流媒体服务在线消费音乐时，很容易忘记实体媒体上的录音时代，也很容易忽略在我们的高保真系统中争夺播放空间的过多竞争格式。[Andrew Rossignol]作为一名 chiptune 爱好者，他对过时的记录媒体格式很有眼光，因为他不仅发现了一台 20 世纪 90 年代的 DAT 机器，[他还黑掉了它以记录高清视频而不是高保真音频](http://www.theresistornetwork.com/2019/02/datvideo-storing-video-on-digital-audio.html)。

如果你以前没有遇到过 DAT，最好把它的格式看作是 CD 播放器的等价物，但是是在磁带上。它起源于 20 世纪 80 年代，使用类似于录像机的螺旋扫描机制在磁带上存储未压缩的 16 位 CD 质量的立体声音频数据流。由于设备的复杂性，它非常昂贵，音乐行业讨厌它，因为他们认为它会被用来制作盗版光盘。尽管有这些障碍，它还是在富有的音乐家和音响发烧友中为自己建立了一个利基市场。如果任何黑客读者遇到了 DAT 磁带，它很可能除了计算机数据之外根本不包含音频，在 20 世纪 90 年代，服务器使用 DAT 磁带进行备份是很常见的。

[Andrew]的黑客行为包括使用他的索尼 DAT 播放器上的 SPDIF 数字接口来传输压缩视频数据。SPDIF 是一个成熟且广为人知的标准，据他计算，其带宽为 187.5 kB/s，足以传输使用 H.265 压缩方案的高清视频。SPDIF 的数据通过 USB 声卡输入电脑，从那里他的软件可以播放或检索视频。该流按照 [RFC1662](https://tools.ietf.org/html/rfc1662) 格式编码成帧，以确保同步，他在下面的视频中进行了演示，并给出了完整的解释。

 [https://www.youtube.com/embed/mOug4t5r0P4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/mOug4t5r0P4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[安德鲁]以前在这里出现过一两次，最引人注目的是他的[卡迪拉克 PHEV](https://hackaday.com/2018/02/22/obd-sniffing-a-caddy-phev/) 。