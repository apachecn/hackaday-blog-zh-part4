# 易于使用的音乐播放器依赖 RFID

> 原文：<https://hackaday.com/2020/08/29/easy-to-use-music-player-relies-on-rfid/>

微波炉过去很容易使用。将刻度盘设置为所需的时间，然后点击开始。然后，一切都数字化了，现在平均每个微波炉需要精确地按下 4 到 6 个按钮才能开始加热。音乐播放器也走上了类似的道路，那些在黑胶唱片时代长大的人会发现现代数字媒体太难使用了。为了解决这个问题，【ananords】推出了 Juuke，[一款专注于易用性的音乐播放器](https://www.instructables.com/id/Juuke-a-RFID-Music-Player-for-Elderly-and-Kids/)。

Juuke 有一个尽可能简单易用的界面。使用嵌入 RFID 标签的印刷卡选择歌曲——将它们放在 Juuke 上触发播放。音量由一个简单的旋钮控制，仅有的两个按钮用于播放/暂停和随机播放模式。

在下面，一个 Arduino Uno 运行这个节目，连接到一个 RC522 RFID 接口板。音乐由 DFPlayer mini 处理，它从 microSD 卡上下载曲目。DFPlayer 可以直接连接到扬声器，但如果该设备要与外部放大器一起使用，还有一个 3.5 毫米的插孔输出。

这是一个整洁的项目，实际上看起来使用起来很有趣。显然，准备 SD 卡和生产 RFID 卡需要一些时间投入，但最终产品在聚会上使用也会很有趣。我们以前也见过类似的版本。休息后的视频。

 [https://www.youtube.com/embed/5Y1Psf6igHE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5Y1Psf6igHE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

