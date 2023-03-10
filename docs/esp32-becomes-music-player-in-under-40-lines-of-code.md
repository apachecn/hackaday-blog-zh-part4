# ESP32 用不到 40 行代码就变成了音乐播放器

> 原文：<https://hackaday.com/2020/06/14/esp32-becomes-music-player-in-under-40-lines-of-code/>

[【XTronical】的基于 ESP32 的 SD 卡音乐播放器](https://www.xtronical.com/esp32mp3/)的演示代码甚至不到 40 行，尽管它还需要一些经济部件才能全部工作。然而，让微控制器从 SD 卡上播放 MP3(和其他格式)比几年前简单多了。

这一切的部分原因是 i2s(IC 间声音)，这是一种用于在设备之间传输 PCM 音频数据的格式。除了 ESP32 之外，它的核心是一个 SD 读卡器分线板和 MAX98357A，它可以被视为 I2S 解码器和 D 类放大器的组合。ESP32 从 SD 卡中读取音频文件，并使用[I2S 音频库](https://github.com/schreibfaul1/ESP32-audioI2S)将 i2s 数据流发送到 MAX98357A(或其中两个用于立体声)。)从那里，它被自动解码，音频通过连接的扬声器传输。

[![](img/c60cc77e51f6b4376fd44b3bc502a3e2.png)](https://hackaday.com/wp-content/uploads/2020/06/ESP32_I2S_PCM5102A.jpg)

A few economical components, and only a handful of connections between them.

令人惊讶的是，当人们可以利用数字方式随机播放音频数据时，音频处理起来会容易得多，解码器可以处理多种格式，内置放大器。在下面嵌入的视频中，您可以看到[XTronical]的 ESP32 播放器正在运行。

 [https://www.youtube.com/embed/Fa5f8IvyqoA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Fa5f8IvyqoA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



对 I2S 感兴趣并想了解更多？你很幸运，因为[我们涵盖了你想知道的关于 I2S 的一切及其运作方式](https://hackaday.com/2019/04/18/all-you-need-to-know-about-i2s/)。