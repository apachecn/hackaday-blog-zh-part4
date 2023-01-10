# GGWave 唱出你的数据之歌

> 原文：<https://hackaday.com/2022/07/06/ggwave-sings-the-songs-of-your-data/>

我们喜欢替代的数据传输方式，Georgi Gerganov 的 ggwave 让我们笑了。其核心是，它在做过去电话调制解调器所做的事情——发送编码为不同音频的数据。但是 GGwave 做这个很老练！

它将数据分成四位块，并使用 16 种不同的频率偏移来表示每个可能的值。但是对于每个组块，这些偏移被添加到六个不同基频中的一个，这允许接收计算机辨别它在哪个组块中。这就像一个简单的框架概念，它使结果数据听起来像 R2-D2 一样迷人。(它还使用开始和结束标记来双重确认帧。)发送的数据还带有纠错功能，因此小问题可以自动修复。

真正让 ggwave 大放异彩的是它被移植到你所关心的每一个平台上:ESP32、Arduino、Linux、Mac、Windows、Android、iOS 以及任何可以运行 Python 或 JavaScript 的平台。所以它可以在浏览器中运行。甚至还有一个图形用户界面，可以玩不同的调制方案。Pshwew！这使得一个极简的基于微控制器的寻呼机按钮很容易控制你的桌面，反之亦然。ESP32 有助于建立物联网风格的 WiFi-音频桥梁。在你的手机上写代码，你可以把它广播给任何一个监听的微控制器。无论您的用例是什么，它都可能包含在内。

现在是不利的一面。数据传输速度很慢，大约每秒 64-160 位，传输必然是不稳定的，除非你用超声波或使用射频 HackRF 演示。但是，当您的设备相互通话时，您可能想听到声音？或者也许你只是觉得很可爱？我们有，但是我们不想用这种方式传输兆字节。但对于一个简单的通知、几个字节的数据、一个 URL 或一些配置参数，我们可以看到这是任何具有扬声器和/或麦克风的设备的一个很好的软件补充。

哦，我的上帝，看看这个链接:[一个 Arduino 的引导程序](https://hackaday.com/2011/09/09/program-an-arduino-using-your-sound-card/)运行在线路上。

 [https://www.youtube.com/embed/aj_GLBtU3Vw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/aj_GLBtU3Vw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

